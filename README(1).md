# Credit Card Fraud Detection

A machine learning practice project for detecting fraudulent credit card transactions using **Logistic Regression**.

## Project Overview

The dataset contains credit card transaction records with a binary `Class` target:

- `0` → Normal / Legitimate transaction
- `1` → Fraudulent transaction

The notebook demonstrates:

1. Importing the required Python libraries
2. Loading the dataset into a Pandas DataFrame
3. Checking dataset information and missing values
4. Exploring the distribution of legitimate and fraudulent transactions
5. Separating legitimate and fraudulent transactions
6. Handling the highly imbalanced dataset using **Under-Sampling**
7. Creating a balanced dataset
8. Splitting features and target
9. Splitting the data into training and testing sets
10. Training a **Logistic Regression** model
11. Evaluating the model using accuracy score

## Dataset

The notebook expects the dataset file to be named:

```text
creditcard.csv
```

The dataset used in the notebook contains:

- **284,807 rows**
- **31 columns**
- **30 feature columns**
- **1 target column: `Class`**
- Legitimate transactions: **284,315**
- Fraudulent transactions: **492**

The original dataset is highly imbalanced, so the notebook uses under-sampling to select **492 legitimate transactions** and combines them with the **492 fraudulent transactions**.

This produces a balanced dataset of **984 transactions**.

> `creditcard.csv` is intentionally excluded from this GitHub repository through `.gitignore`. Add the dataset locally in the project folder before running the notebook.

## Model

**Algorithm:** Logistic Regression

The balanced dataset is split using:

- Test size: **20%**
- `stratify=Y`
- `random_state=2`

Resulting shapes:

- Training data: **787 samples, 30 features**
- Test data: **197 samples, 30 features**

## Results

| Evaluation | Accuracy |
|---|---:|
| Training Accuracy | **95.04%** |
| Test Accuracy | **94.42%** |

The test accuracy is approximately **94.42%**.

## Important Note

The notebook currently produces a `ConvergenceWarning` from scikit-learn because Logistic Regression reaches the default `max_iter=100` limit.

For future improvement, the model can be experimented with using a higher `max_iter` value and/or feature scaling.

## Project Structure

```text
credit-card-fraud-detection/
│
├── credit_cart_fraud_detection.ipynb
├── creditcard.csv              # Not uploaded to GitHub
├── README.md
├── requirements.txt
└── .gitignore
```

## Installation

Create a Python environment and install the dependencies:

```bash
pip install -r requirements.txt
```

## Run the Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
credit_cart_fraud_detection.ipynb
```

Make sure `creditcard.csv` is present in the same project directory before running the notebook.

## Skills / Concepts Practiced

- Python
- NumPy
- Pandas
- Data preprocessing
- Exploratory data analysis
- Handling imbalanced datasets
- Under-sampling
- Train-test split
- Logistic Regression
- Model evaluation
- Accuracy score
- Jupyter Notebook
- Git & GitHub

## Disclaimer

This is a learning/practice machine learning project. The reported accuracy is based on the workflow and notebook outputs included in this repository.
