# Counterfeit IC Detection System

This project aims to detect counterfeit integrated circuits (ICs) using deep learning models such as VGG16, ResNet50, and custom convolutional neural networks (CNN). The dataset includes images of authentic and counterfeit ICs, and the models are trained to classify the ICs based on these images.

## Introduction

Counterfeit ICs pose significant risks to the integrity and reliability of electronic systems across industries. Detecting counterfeit ICs is critical to ensuring product quality and reducing the economic losses incurred by counterfeit goods.

This project explores various deep learning techniques to build a reliable detection system that classifies ICs as either authentic or counterfeit based on image data.

## Project Overview

The core idea behind this project is to develop a robust model that can classify counterfeit ICs based on visual image features. The following steps were performed:

1. **Data Collection**: A dataset of IC images with labels (authentic or counterfeit) was used.
2. **Data Preprocessing**: Images were resized, normalized, and augmented to increase the dataset size.
3. **Model Training**: Multiple deep learning models, including VGG16, ResNet50, and a custom CNN, were trained.
4. **Model Evaluation**: The models were evaluated based on accuracy, precision, recall, and F1-score.

## Dataset

- The dataset consists of 85 images of integrated circuits (ICs), where:
    - 50 images are labeled as authentic (Class “A”).
    - 35 images are labeled as counterfeit (Class “C”).
- Each image has dimensions of 1920x2560 or 1920x2465 pixels and is in RGB format.
- Image types include front and back profiles of the ICs, but these orientations alone do not imply authenticity.

## Models Implemented

The following models were implemented and evaluated:

- **Custom Convolutional Neural Network (CNN)**: Initially implemented but showed underfitting with low accuracy (~58%).
- **ResNet50**: Improved performance but resulted in overfitting with accuracy stagnating around 60%.
- **VGG16**: Achieved the best results with 88% validation accuracy and 98.5% training accuracy.

### Summary of VGG16 Layers:

- Input Layer: (None, 480, 640, 3)
- Convolutional Layers: 13 convolutional layers with 3x3 filters, followed by max-pooling layers.
- Fully Connected Layers: 2 dense layers followed by a final output layer for binary classification.
- Activation Functions: ReLU for hidden layers, Sigmoid for the output layer.

## Preprocessing and Data Augmentation

Given the small size of the dataset, data augmentation was applied to artificially increase the number of training samples:

Augmentation Techniques:
  - Horizontal and vertical flipping
  - Rotation
  - Random background changes
  - Normalization: Pixel values were normalized to the range [0, 1] to improve model training efficiency.

## Results

The VGG16 model provided the best performance with the following results:

- Training Accuracy: 98.5%
- Validation Accuracy: 88.2%
- Precision (Authentic): 90%
- Recall (Authentic): 90%
- Precision (Counterfeit): 86%
- Recall (Counterfeit): 86%
