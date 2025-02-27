# Handwritten-Digit-Recognition-MNIST-


This script performs two main tasks: training an MNIST digit classification model and enabling image uploads for prediction.

## **1. Training the MNIST Model**
- It loads the MNIST dataset, which contains handwritten digit images (0-9).
- The pixel values are normalized to improve training efficiency.
- A **Convolutional Neural Network (CNN)** is built with:
  - Convolutional layers to extract features.
  - MaxPooling layers to reduce dimensionality.
  - Dense layers for classification.
- The model is compiled using the Adam optimizer and sparse categorical cross-entropy loss.
- It is trained for five epochs and validated on test data.
- The trained model is saved as `mnist_model.h5`.

## **2. Image Upload & Prediction**
- A file upload button is created using `ipywidgets` to allow users to upload an image.
- When an image is uploaded:
  - It is converted to grayscale and resized to 28x28 pixels.
  - The image is normalized and reshaped to match the model’s input format.
  - The trained model predicts the digit using a softmax activation function.
  - The most probable digit is displayed.

This approach allows users to upload handwritten digits for real-time classification using the trained model.
