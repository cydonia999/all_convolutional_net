# TensorFlow implementation of all convolution neural networks[1] on MNIST

# Introduction

[1] proposed all convolutional neural networks and showed that an All-CNN-C model achieved the state of the art on CIFAR-10 classification error.

But I am not sure that the All-CNN-C model also works well for MNIST data.

This repository contains a TensorFlow implementation of the all conv nets on MNIST.
Codes are heavily based on TensorFlow tutorial [code](https://github.com/tensorflow/models/blob/master/tutorials/image/mnist/convolutional.py) on MNIST.

# Model

Two all conv nets I tried:
 
1. All-CNN-C model `ALL_CNN_C.py`: the same network structure as [1]

2. Smaller model `smaller_all_conv_net.py`: has the smaller number of convolutional layers than All-CNN-C.

# Results

The smaller model achieve 1% test error on MNIST at 10 epoch.
Note that the original [code](https://github.com/tensorflow/models/blob/master/tutorials/image/mnist/convolutional.py) on MNIST achieved 0.8% test error.

On the other hand, the validation error rate of All-CNN-C model is 26.8% after 5 epochs (smaller model 1.4%).
As described in [2], it would be still valid on MNIST that the deeper models have difficulty in being optimized.

# References:

[1] Jost Tobias Springenberg, Alexey Dosovitskiy, Thomas Brox, Martin Riedmiller, Striving for Simplicity: The All Convolutional Net, [arXiv](https://arxiv.org/abs/1412.6806)

[2] Rupesh Kumar Srivastava, Klaus Greff, Jürgen Schmidhuber, Highway Networks. [arXiv](https://arxiv.org/abs/1505.00387)

[3] [All-Convnet-TensorFlow-MNIST-Tutorial](https://github.com/loliverhennigh/All-Convnet-TensorFlow-MNIST-Tutorial)
