# Machine Learning Classification Project

> A comparative study of machine learning models for binary classification on an imbalanced dataset.

## Project Overview

This project investigates the performance of several machine learning algorithms on a binary classification task. The dataset contains missing values, categorical attributes, and significant class imbalance, making it a realistic machine learning problem.

The goal is to correctly classify samples into:

*  **Circle**
*  **Square**

while maximizing the **F1-score of the minority class**.

---

## Dataset

| Property             | Value           |
| -------------------- | --------------- |
| Samples              | 4,480           |
| Numerical Features   | 10              |
| Categorical Features | 1               |
| Target Classes       | Circle / Square |

### Challenges

* Missing values in multiple features
* Class imbalance
* Mixed numerical and categorical data

---

## Data Preprocessing

The following preprocessing pipeline was applied:

*  Missing value imputation
*  One-Hot Encoding
*  Feature Scaling
*  Class balancing using SMOTE / SMOTE-Tomek
*  Hyperparameter tuning with Grid Search
*  Decision threshold optimization

---

## Models Evaluated

### Support Vector Machine (SVM)

* RBF Kernel
* SMOTE-Tomek balancing
* Grid Search optimization

| Metric   | Score     |
| -------- | --------- |
| F1-Score | **0.63**  |
| Accuracy | **94.9%** |

---

### Decision Tree

* Entropy criterion
* Cost-complexity pruning
* SMOTE oversampling

| Metric   | Score     |
| -------- | --------- |
| F1-Score | **0.51**  |
| Accuracy | **90.7%** |

---

### Neural Network (MLP)

* Multi-Layer Perceptron
* Polynomial feature expansion
* SMOTE-Tomek balancing

| Metric        | Score     |
| ------------- | --------- |
| Validation F1 | **0.68**  |
| Accuracy      | **95.0%** |

---

### XGBoost

* Gradient Boosted Trees
* Class-weight adjustment
* Threshold optimization

| Metric              | Score    |
| ------------------- | -------- |
| Cross-Validation F1 | **0.68** |
| Kaggle Score        | **0.80** |

## Key Findings

* Threshold optimization significantly improved minority-class detection.
* Handling class imbalance was essential for achieving strong F1-scores.
* Ensemble methods outperformed traditional single-model approaches.
* XGBoost achieved the strongest overall performance.

---

## Technologies

```text
Python
Pandas
NumPy
Scikit-Learn
Imbalanced-Learn
XGBoost
```
