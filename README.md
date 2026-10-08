# Telecom Customer Churn Prediction Using Logistic Regression

## Overview

This project focuses on predicting customer churn in a telecom company using the **Telco Customer Churn dataset**.

The main goal is to analyze customer behavior and build a **Machine Learning model** that can identify customers who are likely to leave the company so that proactive customer retention strategies can be applied in time.

---

## Problem Statement

Customer churn is a major challenge for telecom companies. When customers leave, the company loses recurring revenue and needs to spend additional resources to acquire new customers.

The objective of this project is to build a classification model that can predict whether a customer is likely to **churn or stay** based on their demographic information, services, contract details, payment method, tenure, and charges.

---

## Objectives

- Analyze the telecom customer dataset.
- Identify customer attributes related to churn.
- Clean and preprocess the dataset.
- Convert categorical variables into numerical values.
- Build a Logistic Regression classification model.
- Predict the probability of customer churn.
- Classify customers as:
  - Likely to Churn
  - Likely to Stay
- Evaluate model performance using classification metrics.
- Analyze False Positives and False Negatives.
- Interpret the results from a business perspective.
- Suggest an improvement to make churn prediction more reliable.

---

## What I Did

- Loaded and explored the telecom customer dataset using Python and Pandas.
- Checked the dataset structure, missing values, and data types.
- Identified important customer attributes related to churn, such as tenure, contract type, payment method, monthly charges, total charges, and service usage.
- Cleaned and prepared the dataset for machine learning.
- Converted categorical variables into numerical values using encoding.
- Separated the target variable (`Churn`) from the input features.
- Split the dataset into training and testing sets.
- Applied feature scaling using `StandardScaler`.
- Built a **Logistic Regression** model to predict customer churn.
- Predicted the probability of customer churn.
- Classified customers into:
  - Likely to Churn
  - Likely to Stay
- Evaluated the model using:
  - Accuracy
  - Precision
  - Recall
  - F1-Score
  - Confusion Matrix
  - ROC-AUC
- Analyzed the model results from a business perspective.
- Studied the impact of False Positives and False Negatives.
- Suggested adjusting the classification threshold as a possible improvement.

---

## Machine Learning Model

### Logistic Regression

Logistic Regression was used because customer churn is a **binary classification problem**.

The model predicts two possible outcomes:

- `No` → Customer is likely to stay
- `Yes` → Customer is likely to churn

The model also provides the probability of churn, which can help the company prioritize high-risk customers for retention campaigns.

---

## Model Performance

The Logistic Regression model achieved the following results on the test dataset:

| Metric | Score |
|---|---:|
| Accuracy | 77.97% |
| Precision | 69.75% |
| Recall | 30.21% |
| F1-Score | 42.16% |

### Interpretation

The model achieved an overall accuracy of **77.97%**.

However, the **Recall for churn customers is 30.21%**, which means the model is missing a significant number of customers who actually churn.

Therefore, the model should be improved before being used as the only decision-making tool for customer retention campaigns.

---

## Confusion Matrix

The confusion matrix was used to analyze correct and incorrect predictions.

### True Positive (TP)

Customers who actually churned and were correctly predicted as churn.

### True Negative (TN)

Customers who actually stayed and were correctly predicted as stay.

### False Positive (FP)

Customers who actually stayed but were incorrectly predicted as churn.

### False Negative (FN)

Customers who actually churned but were incorrectly predicted as stay.

For customer retention, **False Negatives can be particularly important** because the company may fail to identify a customer who is actually going to leave.

---

## Business Importance

Customer churn prediction can help telecom companies identify at-risk customers early and take proactive retention actions.

Possible retention strategies include:

- Personalized offers
- Discounts
- Loyalty benefits
- Suitable service plans
- Improved customer support
- Targeted retention campaigns

The model can help the company prioritize customers who have a higher probability of churn.

---

## Suggested Improvement

One improvement is to **adjust the classification probability threshold**.

The default threshold of `0.5` can be changed based on the business requirement.

For example, using a lower threshold may help identify more potential churn customers and improve Recall.

However, lowering the threshold may also increase False Positives.

Therefore, the company should select a threshold based on the cost of losing a customer compared with the cost of providing a retention offer.

---

## Tools and Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## Project Workflow

```text
Dataset
   ↓
Data Understanding
   ↓
Data Cleaning
   ↓
Missing Value Handling
   ↓
Feature Selection
   ↓
Categorical Encoding
   ↓
Train-Test Split
   ↓
Feature Scaling
   ↓
Logistic Regression
   ↓
Churn Probability Prediction
   ↓
Churn / Stay Classification
   ↓
Model Evaluation
   ↓
Business Interpretation
