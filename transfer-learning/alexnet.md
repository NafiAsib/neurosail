# AlexNet

`Local Response Normalization (LRN)` is a technique used in convolutional neural networks (CNNs), including AlexNet, to introduce a form of normalization within the network architecture.

LRN is `applied after the activation function in specific layers and aims to enhance the model's generalization capabilities`

The main idea behind LRN is to provide local competition between adjacent channels in the feature maps. It normalizes the responses of neurons across neighboring channels, aiming to enhance the model's response to more prominent features and suppress responses to less salient features. Here's how LRN works:

1. Local neighborhood: For each location in the feature maps, a local neighborhood is defined. This neighborhood includes responses from nearby channels in a specified window size.

2. Normalization: For each neuron, the response is divided by the sum of squares of the responses within the local neighborhood. The purpose of this division is to normalize the response based on the activations of neurons in the vicinity.

3. Scaling: After the normalization step, a scaling parameter (usually a small positive constant) is applied to the normalized response. This scaling term helps control the impact of the normalization on the overall response.

**The key effect of LRN is to introduce a form of lateral inhibition or competition between neighboring channels. By normalizing responses based on the activity of nearby channels, LRN promotes the idea of contrast enhancement. This means that neurons with larger responses relative to their neighbors are emphasized, while those with smaller responses are suppressed. This competitive mechanism encourages the network to respond more strongly to distinct features and enhances the model's ability to generalize to different inputs.**

It's worth noting that LRN has been somewhat less commonly used in recent years, with techniques like batch normalization gaining popularity. However, LRN played a significant role in the original AlexNet architecture and demonstrated its potential benefits in improving model performance on image classification tasks.
