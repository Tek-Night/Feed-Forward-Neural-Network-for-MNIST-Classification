# 🧠 MNIST Feed-Forward Neural Network (From Scratch)

> “I Built a Neural Network from Scratch”

This project implements a **Feed-Forward Neural Network (FFNN)** using only **NumPy**, without TensorFlow, PyTorch, or any deep learning libraries.

The goal is to understand how neural networks work internally by manually implementing every major component — forward pass, backpropagation, and gradient descent.

---

## 📌 Objective

Build a simple neural network to classify handwritten digits from the **MNIST dataset**, while fully understanding the mathematics behind:

- Linear transformations
- ReLU activation
- Softmax activation
- Categorical Cross-Entropy loss
- Backpropagation
- Mini-batch Gradient Descent

---

## 🏗 Model Architecture


Input Layer (784 neurons)
↓
Hidden Layer (Fully Connected + ReLU)
↓
Output Layer (10 neurons + Softmax)


- **Input size:** 784 (28×28 image flattened)
- **Hidden layer:** Fully connected with ReLU activation
- **Output layer:** 10 neurons (digits 0–9) with Softmax
- **Loss function:** Categorical Cross-Entropy
- **Optimizer:** Mini-batch Gradient Descent

---

## ⚙️ Features Implemented

✔ Forward pass computation  
✔ Manual backpropagation  
✔ Gradient calculation for weights and biases  
✔ Weight updates using gradient descent  
✔ Mini-batch training  
✔ Training loss tracking  
✔ Training accuracy tracking  
✔ Visualization of predictions  

---

## 🧮 Mathematical Concepts Used

### Forward Pass

\[
Z^{(1)} = XW^{(1)} + b^{(1)}
\]

\[
A^{(1)} = ReLU(Z^{(1)})
\]

\[
Z^{(2)} = A^{(1)}W^{(2)} + b^{(2)}
\]

\[
\hat{Y} = Softmax(Z^{(2)})
\]

---

### Loss Function (Categorical Cross-Entropy)

\[
L = -\sum y \log(\hat{y})
\]

---

### Backpropagation

Using the Softmax + Cross-Entropy simplification:

\[
\frac{\partial L}{\partial Z^{(2)}} = \hat{Y} - Y
\]

Gradients are computed manually and weights are updated using:

\[
W = W - \eta \nabla W
\]

---

## 📊 Training

The model is trained using **mini-batch gradient descent**.

Why mini-batch?
- More stable than stochastic gradient descent
- Faster than full batch gradient descent
- Reduces noisy updates
- Improves convergence behavior

---

## 📈 Example Results

- Model successfully learns digit classification
- Training loss decreases over epochs
- Accuracy improves steadily
- Correct and incorrect predictions are visualized

---

## 🚀 Why This Project Matters

Most neural network tutorials hide complexity behind frameworks.

This project:
- Builds everything from scratch
- Strengthens mathematical intuition
- Develops real understanding of backpropagation
- Bridges linear algebra with machine learning

---

## 📂 Project Structure


.
├── data/
├── model.py
├── train.py
├── utils.py
└── README.md


---

## 🛠 Requirements


numpy
matplotlib


Install with:

```bash
pip install numpy matplotlib
🎯 Future Improvements

Add multiple hidden layers

Implement He/Xavier initialization

Add learning rate scheduling

Implement momentum or Adam optimizer

Add validation set tracking

👨‍💻 Author

Built as part of a journey to deeply understand Machine Learning fundamentals.

⭐ If You Found This Useful

Give the repository a star ⭐
It motivates further open-source ML projects.