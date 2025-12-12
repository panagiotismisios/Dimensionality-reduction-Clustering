# Dimensionality Reduction and Clustering on Fashion-MNIST

This repository contains the implementation and evaluation of **dimensionality reduction** and **clustering** techniques applied to the **Fashion-MNIST** dataset.  
The project was developed as part of a **Machine Learning** course assignment.

---

## 📌 Project Overview

The objective of this project is to:
- Apply dimensionality reduction techniques on image data
- Perform unsupervised clustering
- Compare clustering performance using standard evaluation metrics

### Dimensionality Reduction Techniques
- **Raw data** (baseline)
- **PCA** – Principal Component Analysis
- **LDA** – Linear Discriminant Analysis
- **SAE** – Stacked Autoencoders

### Clustering Algorithms
- **MiniBatch K-Means**
- **DBSCAN**
- **Agglomerative Clustering**

Dataset used: **Fashion-MNIST** (28×28 grayscale images, 10 classes)

---

## 📂 Repository Structure

├── assignment_2.py # Main experiment pipeline  
├── assignment-2-report.pdf # Detailed project report  
├── Evaluation.csv # Exported evaluation results  
└── README.md # Project documentation


---

## ⚙️ Methodology

### Data Preprocessing
- Pixel normalization to `[0, 1]`
- Flattening images to 784-dimensional vectors
- Train / validation / test split

### Evaluation Metrics
- Calinski–Harabasz Index
- Davies–Bouldin Index
- Silhouette Score
- Adjusted Rand Index (ARI)
- Execution time
- Number of detected clusters

---

## 🧠 Stacked Autoencoder Architecture

| Layer | Neurons | Activation |
|------|--------|------------|
| Encoder 1 | 512 | ReLU |
| Encoder 2 | 128 | ReLU |
| Bottleneck | 2 | Linear |
| Decoder 1 | 128 | ReLU |
| Decoder 2 | 512 | ReLU |
| Output | 784 | Sigmoid |

**Training parameters**
- Loss: Mean Squared Error
- Optimizer: Adam
- Epochs: 10
- Batch size: 64

---

## ▶️ How to Run

### Requirements
```bash
git clone https://github.com/panagiotismisios/Dimensionality-Reduction-and-Clustering-on-Fashion-MNIST

pip install numpy pandas matplotlib scikit-learn tensorflow keras

python assignment_2.py
```

---

## 📊 Key Results

- SAE provides the best low-dimensional representation

- MiniBatch K-Means + SAE achieves the strongest overall clustering performance

- LDA performs well but requires labeled data

- DBSCAN struggles on raw data but detects additional structure after SAE

- Dimensionality reduction significantly reduces clustering execution time

- Detailed analysis and plots are available in the report.

---

## 📄 Report

A complete explanation of:

- Theory

- Parameter selection

- Experimental results

- Visualizations

- Conclusions

is provided in:

📘 **assignment-2-report.pdf**

---

## 📚 References

- Burkov, A. The Hundred-Page Machine Learning Book

- Hastie, Tibshirani, Friedman – An Introduction to Statistical Learning

- TensorFlow Autoencoder Tutorials
