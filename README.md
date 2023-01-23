
# Implementation of Denoising Autoencoder (DAE) Algorithm on CIFAR-10 Dataset
Objective :
*	Apply Unsupervised method of machine learning called Autoencoder which is a type of CNN
*	Understand the impact of changing various parameters in the architecture

##Methodology :
The method being used here is based on the Research paper titled Image Denoising with Color Scheme by Using Autoencoders (Irfan Ali et al, December 2018). 

For understanding the process of autoencoder architecture, CIFAR-10 dataset was used for the entire process. For the learning purpose a simple Gaussian nosie 

##Dataset and Noise
The CIFAR-10 dataset used here consists of 60000 color pictures in 10 classes with 6000 picture per class. Dimension of each image is 32 x 32.
Simple Denoising Autoencoder (DAE)

##MODEL ARCHITECTURE
•	Encoder : 3x3 convolutional layers and downsamping done using 2x2 maxpooling layers
•	Decoder : Upsampling done and layers are symmetric to the encoder.


Each convolutional/deconvolutional layer is followed by a ReLU non-linearity layer
ConvDenoiser(
  (conv1): Conv2d(3, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1))
  (conv2): Conv2d(64, 16, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1))
  (pool): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)
  (t_conv1): ConvTranspose2d(32, 32, kernel_size=(2, 2), stride=(2, 2))
  (t_conv2): ConvTranspose2d(32, 32, kernel_size=(2, 2), stride=(2, 2))
  (convout): Conv2d(32, 3, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1))
)
##Hyperparameters : Batch Size = 32 . no. of epochs = 50 . Learning rate =0.001 .

##Deployment: Since pytorch has inbuilt CIFAR-10 dataset set up in its library, new images have to fed in by converting them to dataloaders for testing.

##OBSERVATIONS:-
Increasing the number of epochs improved the denoising performance
Adding learning scheduler improved the speed of the model.

