# 🧠 Handwritten Digit Classification Using ANN

## 📌 Project Overview

This project implements a **Handwritten Digit Classification** system using an **Artificial Neural Network (ANN)** trained on the well-known **MNIST dataset**.

The objective is to build a neural network capable of recognizing handwritten digits from **0 to 9** using grayscale image pixel values.

Each MNIST image contains a handwritten digit represented as a **28 × 28 pixel** image. The ANN learns patterns from these pixel values and predicts the corresponding digit class.

This project provides a practical introduction to applying **Deep Learning to image classification**.

---

## 🎯 Problem Statement

Given a grayscale image of a handwritten digit, the model must correctly classify it into one of **10 possible classes**:

```text
0, 1, 2, 3, 4, 5, 6, 7, 8, 9
```

The problem is therefore a **multi-class classification task**.

---

## 📊 Dataset

The project uses the **MNIST handwritten digit dataset**, loaded using TensorFlow/Keras:

```python
datasets.mnist.load_data()
```

### Dataset Characteristics

* Image size: **28 × 28 pixels**
* Image type: Grayscale
* Number of classes: **10**
* Classes: `0–9`

Each pixel contains an intensity value representing the brightness of that pixel.

---

## 🔄 Project Workflow

The complete workflow follows:

```text
MNIST Dataset
      ↓
Load Training & Test Data
      ↓
Explore Images
      ↓
Normalize Pixel Values
      ↓
Flatten 28×28 Images
      ↓
Build ANN
      ↓
Train Model
      ↓
Evaluate on Test Data
      ↓
Predict Handwritten Digits
```

---

## 🧹 Data Preprocessing

Before training the neural network, the image data is prepared appropriately.

### 1. Normalization

Pixel values are scaled to a smaller range to make neural network training more stable and efficient.

### 2. Flattening

The original image has a shape of:

```text
28 × 28
```

It is converted into a one-dimensional vector:

```text
784 features
```

This allows the flattened image to be provided to the fully connected ANN.

---

## 🧠 ANN Architecture

The project uses a **feedforward Artificial Neural Network** for multi-class classification.

### Architecture

```text
Input Image
28 × 28 pixels
      ↓
Flatten
784 Features
      ↓
Dense Layer
ReLU Activation
      ↓
Dense Layer
ReLU Activation
      ↓
Output Layer
10 Neurons
Softmax Activation
      ↓
Predicted Digit
0–9
```

### Activation Functions

**ReLU**

ReLU is used in the hidden layers to introduce non-linearity and allow the network to learn complex patterns.

**Softmax**

The output layer uses Softmax because this is a multi-class classification problem. It produces a probability distribution across the 10 digit classes.

---

## Model Training

The ANN is trained using:

* Forward propagation
* Backpropagation
* Gradient-based optimization
* Categorical classification loss
* Multiple training epochs

The network adjusts its weights during training to minimize the difference between the predicted digit probabilities and the actual labels.

---

## Model Evaluation

The model is evaluated on the unseen MNIST test dataset.

### Evaluation Metric

* **Accuracy**

Accuracy provides the percentage of test images correctly classified by the neural network.

The model achieves **high classification performance**, demonstrating that a fully connected ANN can successfully learn useful patterns from handwritten digit images.

---

## Predictions

After training, the model can be used to predict previously unseen handwritten digits.

For each input image, the network produces probabilities for all 10 classes and selects the class with the highest probability.

Example:

```text
Predicted probabilities
       ↓
[0.01, 0.00, 0.02, 0.03, 0.00,
 0.01, 0.00, 0.91, 0.01, 0.01]

Prediction → 7
```

---

## Key Learning

This project demonstrates an important Deep Learning concept:

> **Images can be represented as numerical data, allowing neural networks to learn visual patterns directly from pixel values.**

However, a fully connected ANN does not explicitly understand the spatial relationship between neighboring pixels.

This limitation motivates the use of **Convolutional Neural Networks (CNNs)**, which are specifically designed to capture spatial patterns in images.

---

## Technologies Used

### Programming Language

* Python

### Libraries & Frameworks

* NumPy
* Pandas
* Matplotlib
* TensorFlow
* Keras

### Development Environment

* Jupyter Notebook
* Kaggle Notebook

---

## Project Structure

```text
handwritten-digit-classification-ann/
│
├── handwritten-digit-classification-ann.ipynb
├── README.md
└── dataset/
```

> The MNIST dataset is loaded directly through TensorFlow/Keras and does not need to be manually downloaded.

---

## Learning Outcomes

Through this project, I gained practical experience with:

* MNIST dataset
* Image preprocessing
* Pixel normalization
* Image flattening
* Artificial Neural Networks
* Dense layers
* ReLU activation
* Softmax activation
* Multi-class classification
* Categorical cross-entropy
* Backpropagation
* Model evaluation
* Handwritten digit prediction

---

## Future Improvements

Possible improvements include:

* Implementing a **Convolutional Neural Network (CNN)**
* Comparing ANN and CNN performance
* Adding a confusion matrix
* Visualizing incorrectly classified images
* Adding Dropout regularization
* Experimenting with Batch Normalization
* Hyperparameter tuning
* Data augmentation
* Building an interactive digit prediction application
* Deploying the model using Streamlit

---

## Final Takeaway

This project demonstrates how an **Artificial Neural Network can learn to classify handwritten digits directly from image pixel values**.

Although a fully connected ANN can achieve strong performance on MNIST, image-specific architectures such as **CNNs** can better capture spatial relationships and are generally more suitable for computer vision tasks.

This project therefore serves as a practical foundation for progressing from basic neural networks toward **Computer Vision and Deep Learning architectures**.
