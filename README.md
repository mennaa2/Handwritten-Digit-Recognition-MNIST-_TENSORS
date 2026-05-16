# 🧠 Neural Network Project - Handwritten Digit Recognition (MNIST)

---

## 📌 Project Overview
This project implements a Multilayer Perceptron (MLP) neural network to classify handwritten digits (0–9) using the MNIST dataset.

Multiple experiments were conducted using different activation functions and neuron sizes to compare performance and achieve the best accuracy.

---

## 📊 Dataset

**Name:** MNIST Dataset  
**Link:** https://keras.io/api/datasets/mnist/

### 🎯 Target Classes:
0 → Zero  
1 → One  
2 → Two  
3 → Three  
4 → Four  
5 → Five  
6 → Six  
7 → Seven  
8 → Eight  
9 → Nine  

### 📦 Dataset Size:
- 60,000 training images  
- 10,000 testing images  
- Image size: 28×28 grayscale  

---

## ⚙️ Data Preprocessing

The following preprocessing steps were applied:

✔ Flatten images from 28×28 → 784 vector  
✔ Normalize pixel values (0–255 → 0–1)  
✔ One-hot encoding for labels  
✔ Checked dataset for missing values  

### 🔄 TensorFlow Usage in Data Processing:
The dataset was initially loaded as NumPy arrays and then handled using TensorFlow operations.

Keras (built on TensorFlow) internally works with **tensors**, ensuring efficient computation during training and backpropagation.

Additionally:
- Image reshaping and normalization were performed using tensor-compatible operations
- This ensures compatibility with TensorFlow computation graph

---

## 🧠 Model Architecture

### 🔹 Experiment 1 & 2
- Input Layer: 784 neurons  
- Hidden Layer 1: 128 neurons  
- Hidden Layer 2: 64 neurons  
- Dropout: 0.3  
- Output Layer: 10 neurons (Softmax)

---

### 🔹 Experiment 3
- Input Layer: 784 neurons  
- Hidden Layer 1: 256 neurons  
- Hidden Layer 2: 64 neurons  
- Dropout: 0.3  
- Output Layer: 10 neurons (Softmax)

---

### ⚙️ Techniques Used:
✔ Dropout Regularization  
✔ Adam Optimizer  
✔ Categorical Crossentropy Loss  
✔ TensorFlow / Keras Neural Network Implementation  

---

## 🧪 Experiments Results

| Experiment | Activation | Architecture | Accuracy |
|------------|------------|-------------|----------|
| Exp 1 | ReLU | 128 neurons | 97.38% |
| Exp 2 | Tanh | 128 neurons | 97.22% |
| Exp 3 | ReLU | 256 neurons | 97.98% |

---

## 📈 Results Summary

✔ ReLU outperformed Tanh due to better gradient flow  
✔ Increasing neurons improved learning capacity  
✔ Dropout helped reduce overfitting  
✔ Experiment 3 achieved the best performance  

---

## 📊 Visualizations Included

- Loss Comparison Graph  
- Accuracy Comparison Graph  
- Confusion Matrix for each experiment  

---

## 🏁 Conclusion

The MLP model successfully achieved high accuracy in handwritten digit classification.

### Key Findings:
✔ Activation functions significantly affect performance  
✔ Larger networks improve feature learning  
✔ Dropout improves generalization  

---

## 🏆 Best Model

**Experiment 3**

- Activation: ReLU  
- Neurons: 256  
- Epochs: 20  
- Accuracy: ~97.98%  

---

## ⚙️ How to Run

### Install dependencies:
```bash
pip install tensorflow matplotlib scikit-learn numpy
