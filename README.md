This project implements an image classification model on the CIFAR-10 dataset.
The dataset contains 60,000 color images (32×32×3 pixels) across 10 classes such as airplanes, cars, birds, cats, and more.
Two models were experimented with:
A simple Artificial Neural Network (ANN) built using fully connected layers:
Flatten → Dense(3000, ReLU) → Dense(1000, ReLU) → Dense(10, Softmax)
A more powerful Convolutional Neural Network (CNN) that forms the core of this project.
The CNN architecture consists of:
Input layer that takes (32,32,3) images,Two convolutional layers: Conv2D(32, 3×3, ReLU) and Conv2D(64, 3×3, ReLU)
Each convolutional layer is paired with MaxPooling2D(2×2) for feature downsampling
A Flatten layer,Two dense layers: Dense(64, ReLU) and Dense(10, Softmax) for classification
The model is compiled with:Adam optimizer and Sparse categorical crossentropy loss
Training was done for 5 epochs on the CIFAR-10 training set. Overall, this notebook demonstrates:
The effectiveness of CNNs in automatically learning hierarchical visual features
A comparison with simple dense-layer ANNs
How convolution + pooling operations capture spatial patterns for robust image recognition
