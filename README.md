# Employee Attrition Prediction Using Advanced Machine Learning Models

## Overview
This project addresses the challenge of employee attrition at a large corporation. Leveraging data from the Human Resources department, the goal is to predict whether an employee is likely to leave the company. A deep analysis is performed to identify the key drivers behind employee turnover, followed by the construction of machine learning models to make accurate predictions. By identifying at-risk employees early, companies can intervene with retention strategies, ultimately reducing turnover costs.

## Problem Statement
High employee turnover is a critical issue for most organizations, leading to increased costs related to recruiting, onboarding, and training new employees. The objective of this project is to build a predictive model that accurately forecasts whether an employee is likely to leave the company based on features such as satisfaction level, workload, number of projects, and salary.

## Dataset
The dataset contains 14,999 employee records with 10 features:
- `satisfaction_level`: Employee satisfaction score (0–1)
- `last_evaluation`: Last performance review score (0–1)
- `number_project`: Number of projects the employee is involved in
- `average_monthly_hours`: Average hours worked per month
- `time_spend_company`: Years spent at the company
- `work_accident`: Whether the employee had a work accident (binary)
- `left`: Whether the employee left the company (target variable)
- `promotion_last_5years`: Whether the employee was promoted in the last 5 years
- `Department`: Employee department
- `salary`: Employee salary level (low, medium, high)

## Project Workflow

### 1. Data Cleaning:
- Removed duplicates (20% of the data was duplicated).
- Handled categorical variables and feature engineering, such as creating an `overworked` feature to capture employees working more than 250 hours per month.

### 2. Exploratory Data Analysis (EDA):
- A thorough exploration to understand relationships between key variables, including satisfaction level, tenure, and workload.
- Visualizations like correlation heatmaps, bar plots, and scatterplots provide insights into the data.

### 3. Feature Engineering:
- Binned satisfaction levels into low, medium, and high.
- Added a binary `overworked` feature based on monthly hours worked.
- One-hot encoded categorical variables like department and salary to feed into the models.

### 4. Model Selection & Tuning:
- **Logistic Regression**: Used as a baseline model but struggled with non-linear relationships.
- **Random Forest**: A tree-based model that captured feature importance well and achieved high accuracy.
- **XGBoost**: A more advanced ensemble model with the best performance after hyperparameter tuning using GridSearchCV.

### 5. Evaluation:
- Models were evaluated based on accuracy, precision, recall, F1-score, and AUC (Area Under the Curve). Both Random Forest and XGBoost outperformed Logistic Regression.

## Insights and Recommendations
The model identified key drivers of employee attrition, such as low job satisfaction, overwork, and lack of promotions. Actionable insights were derived for the HR department to reduce turnover rates.

## Key Findings
**Feature Importance (from XGBoost and Random Forest):**
- **Satisfaction Level**: Employees with satisfaction below 0.4 are significantly more likely to leave.
- **Overworked**: Employees working more than 250 hours per month are at higher risk of leaving.
- **Tenure**: Employees with 3–4 years at the company have the highest attrition rates, especially if they have not been promoted.

## Conclusion
The XGBoost model was the best performing model with an AUC of 0.94 and a precision of 92% for predicting employees likely to leave. These insights are critical for HR to take proactive steps in employee retention, such as balancing workloads and addressing job satisfaction.
