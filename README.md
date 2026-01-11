# Handwritten Digit Classification using ANN

## Overview
This project implements a handwritten digit classification system using an Artificial Neural Network (ANN).  
The model is trained on the MNIST dataset to recognize digits from 0 to 9 based on pixel intensity values.

---

## Problem Statement
Given a grayscale image of a handwritten digit (28×28 pixels), the task is to correctly classify it into one of the 10 digit classes (0–9).

---

## Approach
- Flattened image pixels into feature vectors
- Built a feedforward Artificial Neural Network (ANN)
- Used activation functions like ReLU and Softmax
- Optimized using categorical cross-entropy loss
- Evaluated model performance using accuracy

---

## Model Architecture
- Input Layer: 784 neurons (28×28 pixels)
- Hidden Layers: Fully connected dense layers
- Output Layer: 10 neurons (Softmax)

---

## Results
- Achieved high classification accuracy on test data
- Successfully learned digit patterns using ANN

---

## Technologies Used
- Python
- NumPy
- Pandas
- Matplotlib
- TensorFlow / Keras
- Jupyter Notebook

---

## Future Improvements
- Use CNN for better spatial feature learning
- Add confusion matrix visualization
- Experiment with dropout and batch normalization

---
