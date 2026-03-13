---
title: Banking Risk Analytics & Prediction System
author: Mohd Mehtab Mohd Idris Siddiqui
tools:
  - Python
  - Pandas
  - Scikit-Learn
  - XGBoost
  - Machine Learning
  - Power BI
  - Jupyter Notebook
project_type: End-to-End Machine Learning Project
domain: Banking / Financial Risk Analytics
---

# Banking Risk Analytics & Prediction System

## Overview
This project builds an end-to-end machine learning pipeline to analyze banking customer behavior and predict two major financial risks:

1. **Customer Churn Prediction**
2. **Loan Default Prediction**

Both models were developed independently and then integrated into a unified prediction pipeline capable of generating risk insights for a combined banking dataset.

The goal of the project is to demonstrate how machine learning can support **customer retention strategies and credit risk assessment in the banking sector.**

---

# Project Architecture

Data Collection → Data Cleaning → Feature Engineering → Model Training → Model Evaluation → Model Integration → Prediction Pipeline → Analytics Dashboard

---


---

# Model 1: Customer Churn Prediction

## Objective
Predict whether a banking customer is likely to leave the bank.

## Dataset Link
https://www.kaggle.com/datasets/mathchi/churn-for-bank-customers

## Dataset Features
- CreditScore
- Geography
- Gender
- Age
- Tenure
- Balance
- NumOfProducts
- HasCrCard
- IsActiveMember
- EstimatedSalary

## Model Used
Weighted Random Forest Classifier

## Reason for Weighted Model
The dataset contained **class imbalance**, meaning churned customers were significantly fewer than retained customers.  
Class weights were used to improve the model's ability to correctly identify churn cases without significantly sacrificing overall accuracy.

## Key Performance Metrics
- Accuracy: ~83%
- Balanced recall improvement
- Strong classification performance for both churn and non-churn customers

---

# Model 2: Loan Default Prediction

## Objective
Predict whether a borrower is likely to default on a loan.

## Dataset Link
https://www.kaggle.com/datasets/nikhil1e9/loan-default

## Dataset Features
- Income
- LoanAmount
- MonthsEmployed
- NumCreditLines
- InterestRate
- LoanTerm
- DTIRatio
- Education
- EmploymentType
- MaritalStatus
- HasMortgage
- HasDependents
- LoanPurpose
- HasCoSigner

## Models Tested
- Random Forest
- XGBoost

## Final Model Selected
XGBoost Classifier

## Key Performance Metrics
- ROC-AUC: ~0.72
- Improved recall for identifying high-risk borrowers
- Strong ability to detect default cases

---

# Model Integration

After training both models, they were integrated into a **single prediction pipeline**.

The pipeline performs:

1. Load trained models
2. Load new customer dataset
3. Apply required preprocessing
4. Generate predictions from both models
5. Combine results into a single output dataset

### Output Predictions
- Churn Prediction
- Churn Probability
- Loan Default Prediction
- Loan Default Probability

This combined dataset can be used for **risk monitoring and business decision-making**.

---

# Synthetic Dataset Generation

A synthetic banking dataset was generated to simulate new customers for prediction.

The dataset includes both:
- Customer banking features
- Loan related features

Total simulated customers: **120,000**

This dataset was used to test the integrated prediction pipeline.

---

# Business Applications

The system enables banks to:

- Identify customers likely to churn
- Detect high-risk borrowers before loan approval
- Segment customers by financial risk
- Support proactive retention strategies
- Improve credit risk assessment

---

# Future Enhancements

Possible improvements include:

- Hyperparameter tuning for model optimization
- Real banking transaction data integration
- Deployment as an API service
- Real-time risk monitoring dashboard in Power BI
- Customer segmentation analysis

---

# Key Skills Demonstrated

- Machine Learning Model Development
- Handling Imbalanced Datasets
- Feature Engineering
- Model Evaluation & Comparison
- XGBoost Implementation
- Model Integration Pipelines
- Synthetic Data Generation
- Financial Risk Analytics

---
