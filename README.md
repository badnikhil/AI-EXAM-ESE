# 💳 Credit Card Fraud Detection Using Machine Learning

With the exponential rise in digital payments and e-commerce, credit card fraud has become a pressing challenge. This project aims to build a machine learning model that can accurately detect fraudulent transactions using advanced techniques like **SMOTE** for class imbalance and **Random Forest Classifier** for classification.

---

## 📌 Table of Contents

- [Introduction](#introduction)
- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [Methodology](#methodology)
- [Data Preprocessing](#data-preprocessing)
- [Model Implementation](#model-implementation)
- [Evaluation Metrics](#evaluation-metrics)
- [Results and Analysis](#results-and-analysis)
- [Conclusion](#conclusion)
- [References](#references)
- [How to Run](#how-to-run)

---

## 🔍 Introduction

Credit card fraud detection is a major concern for financial institutions and customers. Traditional systems often fail to keep up with the volume and complexity of transactions. In this project, we employ machine learning to detect fraud with a focus on real-time prediction, accuracy, and handling imbalanced data.

---

## 🧠 Problem Statement

To build a classification model that:
- Detects whether a credit card transaction is fraudulent (1) or normal (0)
- Minimizes both false negatives and false positives
- Handles imbalanced datasets using oversampling techniques

---

## 🎯 Objectives

- Load and preprocess the credit card transaction dataset.
- Handle class imbalance using **SMOTE**.
- Train a **Random Forest Classifier**.
- Evaluate using **accuracy, confusion matrix, ROC-AUC**.
- Visualize results using **matplotlib** and **seaborn**.
- Accept **user input** to test the model with custom data.

---

## ⚙️ Methodology

### 1. Dataset
- `creditcard.csv` from Kaggle with anonymized features and labeled transactions.

### 2. Preprocessing
- Drop `Time` column.
- Normalize `Amount` using `StandardScaler`.
- Apply **SMOTE** to oversample the minority class.

### 3. Model Training
- Split data into 80% training and 20% testing.
- Train a **Random Forest Classifier** on balanced data.

### 4. Evaluation
- Use metrics: Accuracy, Confusion Matrix, ROC-AUC
- Visualize performance using seaborn heatmaps and matplotlib charts.

### 5. User Input
- Predict fraud likelihood from manually entered transaction data.

---

## 🧹 Data Preprocessing

```python
# Standardize 'Amount'
scaler = StandardScaler()
data['Amount'] = scaler.fit_transform(data[['Amount']])

# Drop irrelevant 'Time' column
data.drop(['Time'], axis=1, inplace=True)
