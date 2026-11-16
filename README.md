# MNIST Handwritten Digit Classifier (CNN)

A Convolutional Neural Network built with TensorFlow/Keras to recognize handwritten digits (0-9) from the MNIST dataset, reaching **99.09% test accuracy**.

## Results

| Metric | Value |
|---|---|
| Test Accuracy | **99.09%** |
| Test Loss | 0.0300 |
| Training Samples | 60,000 |
| Test Samples | 10,000 |

## Model Architecture

```
Conv2D(32, 3x3, ReLU) -> MaxPooling2D(2x2)
Conv2D(64, 3x3, ReLU) -> MaxPooling2D(2x2)
Flatten
Dense(128, ReLU)
Dense(10, Softmax)
```

- **Optimizer:** Adam
- **Loss:** Categorical Crossentropy
- **Batch size:** 128
- **Callback:** EarlyStopping (monitor `val_loss`, patience 5, restore best weights)

## Workflow

1. Load the MNIST dataset
2. Normalize pixel values to [0, 1] and reshape to (28, 28, 1)
3. One-hot encode labels
4. Build and compile the CNN
5. Train with early stopping
6. Evaluate on the test set and visualize predictions

## Tech Stack

Python, TensorFlow/Keras, NumPy, Matplotlib

## How to Run

```bash
git clone https://github.com/<your-username>/mnist-cnn-digit-classifier.git
cd mnist-cnn-digit-classifier
pip install tensorflow matplotlib numpy
jupyter notebook mnist_cnn.ipynb
```

Or open the notebook directly in Google Colab.

## Author

**Farouk Nasser**
Electronics & Communications Engineering student | Data Science & Machine Learning
