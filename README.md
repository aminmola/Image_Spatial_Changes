# Image_Spatial_Changes

This project implements a deep learning architecture designed to detect spatial changes between two sets of images: an original image and a transformed (manipulated) version of the same image. The model utilizes spatial and channel feature exchange mechanisms to capture and highlight differences between the two inputs, enabling accurate change detection.

Model Architecture
The architecture consists of several key components:

* Stem Layer: A convolutional block used to extract initial features from both the original and changed images.
* Spatial Exchange Module: Exchanges features along the spatial dimension, focusing on differences in regions across the width of the images.
* Channel Exchange Module: Exchanges features across the channel dimension, ensuring detailed feature-level comparisons.
* Residual Blocks: Deep convolutional blocks for further feature extraction, followed by a ReLU activation and dropout for regularization.
* Fully Connected Layer: Following global average pooling, the output is classified using a softmax activation to predict the likelihood of change or no change.

![alt text](<sample.png>)

Test Procedure
The test dataset is used to evaluate the model's final performance after training, where:


* Test accuracy and loss are calculated.
* Predicted and actual labels are saved for further analysis (e.g., confusion matrix generation).
