# Credit Card Fraud Detection 💳

A Machine Learning practice project for detecting fraudulent credit card transactions using **Logistic Regression**.

---

## 📌 Project Overview

Credit card fraud detection is a classification problem where the goal is to identify whether a transaction is **legitimate** or **fraudulent**.

In this project, I used a credit card transaction dataset and built a **Logistic Regression** model to classify transactions.

The dataset is highly imbalanced because fraudulent transactions are much fewer than legitimate transactions.

To handle this problem, **Under-Sampling** was used to create a balanced dataset before training the model.

---

## 🎯 Objective

The main objective of this project is to:

- Understand the credit card transaction dataset
- Explore legitimate and fraudulent transactions
- Handle an imbalanced dataset
- Create a balanced dataset using Under-Sampling
- Train a Logistic Regression classification model
- Evaluate the model using accuracy score

---

## 📂 Dataset

The dataset contains credit card transaction records with a target column named `Class`.

### Target Variable

- `0` → Legitimate Transaction
- `1` → Fraudulent Transaction

### Dataset Information

- Total transactions: **284,807**
- Total columns: **31**
- Features: **30**
- Target column: **Class**
- Legitimate transactions: **284,315**
- Fraudulent transactions: **492**

The dataset is highly imbalanced because the number of fraudulent transactions is very small compared to legitimate transactions.

---

## ⚖️ Handling Imbalanced Dataset

Since the dataset is highly imbalanced, the model could become biased toward legitimate transactions.

To solve this problem, **Under-Sampling** was performed.

From the legitimate transactions, **492 samples** were randomly selected to match the **492 fraudulent transactions**.

This resulted in a balanced dataset containing:

- Legitimate transactions: **492**
- Fraudulent transactions: **492**
- Total balanced transactions: **984**

---

## 🤖 Machine Learning Model

The classification algorithm used in this project is:

### Logistic Regression

Logistic Regression is a supervised machine learning algorithm commonly used for binary classification problems.

In this project, it is used to classify transactions into:

```text
0 → Legitimate
1 → Fraudulent
