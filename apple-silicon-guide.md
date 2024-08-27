# Simple guide to setup Apple Silicon for ML (w/o *conda)

- Setup Python virtual environment

```bash
python3 -m venv .venv # Create virtual environment
source .venv/bin/activate # Activate virtual environment
pip install -U pip      # Upgrade pip
```

- Install packages related to PyTorch

```bash
pip install torch torchvision torchaudio
```

- Install packages related to TensorFlow

```bash
pip install tensorflow tensorflow-macos tensorflow-metal
```

- Install packages related to JAX

```bash
pip install jax-metal ml_dtypes==0.2.0 jax==0.4.26 jaxlib==0.4.26
```