# Dual-CNN

## Table of Contents
    Overview
    Introduction
    Features
    Requirements
    Model Architecture
    Results
## OVERVIEW
This project focuses on the classification of mammograms into malignant and benign categories using a Dual Convolutional Neural Network (Dual CNN). The goal is to assist in the early detection of breast cancer through automated analysis of mammographic images.


## Introduction
Breast cancer is a prevalent health concern worldwide, and early detection significantly improves the chances of successful treatment. This project employs a Dual CNN approach for the automated classification of mammograms, distinguishing between malignant and benign cases. The neural network model is trained on a curated dataset to achieve accurate predictions.

## Features

    1. Dual CNN architecture for improved classification performance.
    2. Easy integration with existing workflows.
    3. Detailed documentation for quick setup and usage.

## Requirements

    Python 3.x
    TensorFlow
    Keras
    NumPy
    Matplotlib
    Pandas
    cv2
    seaborn
    sklearn

## Model Architecture
As the name suggests there are two branches of CNN involved. 
The first one include:
    Convolutional layer with 32 filters, each of size (3, 3), using ReLU activation.
    MaxPooling layer with pool size (2, 2) to down-sample the spatial dimensions.
    Convolutional layer with 64 filters, each of size (3, 3), using ReLU activation.
    Another MaxPooling layer with pool size (2, 2).
    Flatten layer to convert the 2D feature map to a 1D vector.
    Fully connected Dense layer with 128 neurons using ReLU activation.

The second one include:
    Convolutional layer with 32 filters, each of size (5, 5), using ReLU activation.
    MaxPooling layer with pool size (2, 2).
    Convolutional layer with 64 filters, each of size (5, 5), using ReLU activation.
    Another MaxPooling layer with pool size (2, 2).
    Flatten layer.
    Fully connected Dense layer with 128 neurons using ReLU activation.


The outputs of both branches are concatenated, and then there are common dense layers for further processing. The concatenated output is passed through a Dense layer with 256 neurons and ReLU activation, followed by another Dense layer with 128 neurons and ReLU activation.

Finally, the model has an output layer with 2 neurons and a sigmoid activation function, indicating binary classification. The model is compiled with the Adam optimizer, binary crossentropy loss, and accuracy as the metric.

![image](https://github.com/Bhavana7370/Dual--CNN/assets/121118344/db20b1c2-b6b2-4afa-bb5d-5e8761356ff6)



## Results:

![Screenshot from 2024-03-05 21-40-08](https://github.com/Bhavana7370/Dual--CNN/assets/121118344/e6c49db6-94eb-4c9d-a17b-ec6c25013bcf)


![Screenshot from 2024-03-05 21-40-38](https://github.com/Bhavana7370/Dual--CNN/assets/121118344/9b6032bd-a132-49c1-b4db-450e278d5b67)

![image](https://github.com/Bhavana7370/Dual--CNN/assets/121118344/c81f98c1-7d69-47ff-9ec9-5c6a891b47a3)

The final accuracy observed for this particular model was 62.5% 


Number of Epochs: 50
Batch Size: 32
Optimizer: Adam
Loss function: Binary Crossentropy
Metrics: Accuracy

