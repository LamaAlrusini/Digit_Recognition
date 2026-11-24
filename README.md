# Digit_Recognition
Handwritten digit classification using a Convolutional Neural Network (CNN) with TensorFlow and Keras. Includes model evaluation before and after training, training curves, and performance comparison.

# MNIST Digit Recognition using CNN

A handwritten digit recognition project using a **Convolutional Neural Network (CNN)** built with TensorFlow and Keras.

The goal is to train a deep learning model to classify handwritten digits (0–9) and evaluate its performance before and after training.

## Project Overview

This project uses the MNIST dataset, which contains grayscale images of handwritten digits. Each image has a size of 28 × 28 pixels.

The model learns visual patterns and features from the images to predict the corresponding digit.

## Dataset

- **Source:** [MNIST in CSV – Kaggle](https://www.kaggle.com/datasets/oddrationale/mnist-in-csv)
- Image dimensions: 28 × 28 pixels
- Color format: Grayscale
- Number of classes: 10 (digits 0–9)

### Data Split

| Dataset | Number of Images | Purpose |
|---|---:|---|
| Training | 12,000 | Model training |
| Validation | 3,000 | Performance monitoring |
| Testing | 3,000 | Model evaluation |

The training and validation sets are sampled from the original training dataset. The test set is independently sampled from the original test dataset.

## Model Architecture

A Sequential CNN architecture was implemented using TensorFlow/Keras.

| Layer | Configuration |
|---|---|
| Input | 28 × 28 × 1 |
| Conv2D | 32 filters, 3 × 3, ReLU |
| MaxPooling2D | 2 × 2 |
| Conv2D | 64 filters, 3 × 3, ReLU |
| MaxPooling2D | 2 × 2 |
| Flatten | Feature vector |
| Dense | 64 neurons, ReLU |
| Output | 10 neurons, Softmax |

**Training Configuration:**

- Optimizer: Adam
- Loss Function: Sparse Categorical Crossentropy
- Evaluation Metric: Accuracy
- Epochs: 5
- Batch Size: 64

## Results

The model was evaluated using the same test set before and after training.

| Metric | Before Training | After Training |
|---|---:|---:|
| Test Accuracy | 8.20% | **96.80%** |
| Test Loss | 2.3001 | **0.0966** |

The model achieved a significant improvement in classification accuracy after five training epochs, demonstrating its ability to learn meaningful patterns from handwritten digit images.

## Training Curves

The project includes training and validation curves to monitor model performance across epochs:

- Training Loss
- Validation Loss
- Training Accuracy
- Validation Accuracy

## Technologies & Libraries

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- KaggleHub
- Google Colab

## How to Run

1. Open the notebook in Google Colab.
2. Run the cells sequentially.
3. Download the MNIST dataset through KaggleHub.
4. Preprocess and split the dataset.
5. Build and evaluate the CNN before training.
6. Train the model and evaluate it again.
7. Generate the training curves and final performance comparison.

## Project Structure

```text
mnist-digit-recognition-cnn/
│
├── MNIST_Digit_Recognition.ipynb
├── README.md
└── training_curves.png
```

*Note: `training_curves.png` and the trained model file are generated when the notebook is executed.*

## Key Learning Outcomes

- Understanding image classification with CNNs.
- Preparing and normalizing image datasets.
- Understanding training, validation, and testing datasets.
- Building and training a CNN using TensorFlow/Keras.
- Evaluating model performance using loss and accuracy.
- Comparing model performance before and after training.
- Visualizing training and validation curves.
