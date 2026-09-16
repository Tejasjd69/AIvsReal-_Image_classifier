# AIvsReal

AIvsReal is an image classification project that uses the CIFAKE dataset to distinguish between AI-generated and real images. The model is built using a Convolutional Neural Network (CNN) with transfer learning from the ResNet50v2 architecture and customized layers to enhance performance.

## Table of Contents
- [Project Description](#project-description)
- [Features](#features)
- [Model Architecture](#model-architecture)
- [Model Performance](#model-performance)
- [Dependencies](#dependencies)
- [Contribution](#contribution)
- [Conclusion](#conclusion)

## Project Description

AIvsReal is designed to classify images as either AI-generated or real. The project utilizes the CIFAKE dataset, which can be accessed using the Kaggle API.CIFAKE is a dataset that contains 60,000 synthetically-generated images and 60,000 real images (collected from CIFAR-10).The REAL images are collected from the images from Krizhevsky & Hinton's CIFAR-10 dataset.Fake images are generated from equivalent of CIFAR-10 with Stable Diffusion version 1.4.
The model leverages the ResNet50v2 architecture, incorporating custom layers to improve accuracy and performance.

## Features

- **Transfer Learning**: Utilizes ResNet50v2 for efficient and robust feature extraction.
- **Custom Layers**: Includes additional layers for dropout, batch normalization, flattening, and dense connections to enhance model performance.
- **Early Stopping**: Implements early stopping to prevent overfitting and improve generalization.
- **High Accuracy**: Achieves 97.35% training accuracy and 96.14% test accuracy.
- **Performance Metrics**: Provides precision and recall metrics for both training and testing datasets.
- **Confusion Matrix**: Visualizes the classification performance.

## Model Architecture

The model architecture includes:

```

model = Sequential([
    ResNet50V2,
    Dropout(0.25),
    BatchNormalization(),
    Flatten(),
    Dense(64, activation='relu'),
    BatchNormalization(),
    Dropout(0.5),
    Dense(1, activation='sigmoid')
])

```
## Model Performance
- Training Accuracy: 97.35%
- Test Accuracy: 96.14%
- Training Precision: 0.9738
- Training Recall: 0.9732
- Test Precision: 0.9807
- Test Recall: 0.9414
## Dependencies

- TensorFlow
- Keras
- numpy
- pandas
- scikit-learn
- matplotlib
- seaborn
- kaggle
- PIL



## Conclusion
AIvsReal demonstrates the power of transfer learning combined with custom layers in building an effective image classification model. With a high accuracy and robust performance metrics, this project provides a solid foundation for distinguishing between AI-generated and real images. Future improvements could include exploring other architectures, fine-tuning hyperparameters, and expanding the dataset for even better results.

