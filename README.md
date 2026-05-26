# Handwritten Digit Recognition (MNIST)

A **beginner-friendly** Deep Learning project. Train a Neural Network to read handwritten digits (0–9) using MNIST, TensorFlow/Keras, and one Jupyter notebook.

---

## Project files 

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

## What the notebook teaches

1. Load and explore MNIST  
2. Visualize sample digits  
3. Preprocess (normalize, one-hot encode)  
4. Build a Neural Network (Flatten → Dense → Dropout → Softmax)  
5. Train and plot accuracy/loss  
6. Evaluate on test data  
7. Compare predictions vs real labels  
8. Predict on `custom_digit.png` or your own drawing  

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

## Draw your own digit

1. Draw **one digit** in Paint (black on white).  
2. Save as `my_digit.png` in this folder.  
3. In the notebook, run the last cells and use `predict_custom_digit("my_digit.png", invert=True)`.

---

## Common problems

| Problem | Fix |
|---------|-----|
| `No module named 'tensorflow'` | Run `pip install -r requirements.txt`, restart kernel |
| `tensorflow.python` error | Run `pip uninstall tensorflow -y` then `pip install -r requirements.txt` again |
| Pip fails on Windows (long path) | Use Python 3.11, or enable [long paths](https://pip.pypa.io/warnings/enable-long-paths) in Windows settings |
| Wrong custom prediction | Try `invert=True` or `invert=False`; center the digit in the image |

---

## License

Free for learning and practice.
