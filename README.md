# Handwritten Digit Recognition (MNIST)

A **beginner-friendly** Deep Learning project. Train a Neural Network to read handwritten digits (0–9) using MNIST, TensorFlow/Keras, and one Jupyter notebook.

---

## Project files (only these 7)

```
Image/
├── handwritten_digit_recognition.ipynb   # Main notebook — open and run this
├── requirements.txt                      # Python packages to install
├── README.md                             # This guide
├── mnist_train.csv                       # MNIST training data (optional)
├── mnist_test.csv                        # MNIST test data (optional)
├── custom_digit.png                      # Sample image for Step 10
└── mnist_digit_model.keras               # Pre-trained model (use or re-train)
```

The notebook uses **Keras built-in MNIST** by default. The CSV files are extra data you can explore with pandas.

---

## What you need

- Python **3.10, 3.11, or 3.12** (best for TensorFlow on Windows)
- Jupyter Notebook or VS Code 
- About 30 minutes for first run (install + training)

---
## Introduction
MNIST contains 70,000 images of handwritten digits: 60,000 for training and 10,000 for testing. The images are grayscale, 28x28 pixels, and centered to reduce preprocessing and get started quicker.

Keras is a high-level neural network API focused on user friendliness, fast prototyping, modularity and extensibility. It works with deep learning frameworks like Tensorflow, Theano and CNTK, so we can get right into building and training a neural network without a lot of fuss

---



---

## Model (simple view)

| Layer | What it does |
|-------|----------------|
| Flatten | 28×28 image → 784 numbers |
| Dense 128 + ReLU | Learns patterns |
| Dropout 0.2 | Reduces overfitting |
| Dense 64 + ReLU | Learns more patterns |
| Dense 10 + Softmax | Probability for digits 0–9 |

Expected accuracy: **about 97–98%** on the test set.

---

## Accuracy
It achieved 98% of accuracy with this CNN trained on a GPU, which took me about a minute. If you dont have a GPU powered machine it might take a little longer, you can try reducing the epochs (steps) to reduce computation.

It achieved 98.15% of accuracy on test set of this CNN model trained on GPU.
