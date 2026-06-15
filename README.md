# Neural Network From Scratch (MNIST)

A from-scratch implementation of a Multilayer Perceptron (MLP) for handwritten digit classification on the MNIST dataset using only NumPy.

## Features

- Fully connected feedforward neural network
- Forward propagation
- Backpropagation
- Mini-batch gradient descent
- ReLU, Tanh, and Softmax activations
- Dropout regularization
- Early stopping
- One-hot encoded targets
- Training and validation monitoring
- Confusion matrix evaluation

## Dataset

The project uses the MNIST handwritten digit dataset stored as CSV files:

```text
dataset/
├── mnist_train.csv
└── mnist_test.csv
```

Each image consists of 784 pixel values (28×28) and a corresponding digit label (0–9).

## Network Architecture

Several architectures are explored in the notebook, including:

```text
784 → 256 → 10
784 → 256 → 64 → 10
784 → 512 → 128 → 10
```

Example final model:

```text
784 → 512 → 128 → 10
Activations:
ReLU → Tanh → Softmax
```

## Training Configuration

Example hyperparameters:

```python
learning_rate = 0.15
batch_size = 128
epochs = 35
keep_prob = 0.7
```

The notebook also investigates:

- Different learning rates
- Different batch sizes
- Different network depths
- Different hidden layer widths

## Results

The notebook includes:

- Training loss curves
- Validation loss curves
- Accuracy evaluation
- Confusion matrix visualization
- Sample digit visualization

## Requirements

```bash
pip install numpy pandas matplotlib scikit-learn
```

## Running

1. Place the MNIST CSV files inside the `dataset/` directory.
2. Open the notebook:

```bash
jupyter notebook mnist_mlp.ipynb
```

3. Run all cells.

## Project Structure

```text
.
├── mnist_mlp.ipynb
├── dataset/
│   ├── mnist_train.csv
│   └── mnist_test.csv
└── README.md
```

## Educational Purpose

This project was developed as part of a Computational Intelligence course to understand how neural networks work internally without relying on deep learning frameworks such as TensorFlow or PyTorch.
