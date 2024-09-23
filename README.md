# Employee Attrition Prediction Using Advanced Machine Learning Models

## Project Overview
This project focuses on predicting employee retention at Salifort Motors by leveraging advanced machine learning techniques. The objective is to uncover the primary factors influencing employee turnover and provide actionable insights that HR teams can use to increase employee satisfaction and reduce attrition. The analysis explores trends in work-life balance, promotions, job satisfaction, and other key factors that affect retention.

## Dataset
The dataset comprises 14,999 records and 10 features, covering:
- **Job satisfaction**: Employee self-reported satisfaction levels.
- **Performance evaluation**: Latest performance review scores.
- **Number of projects**: Total number of projects an employee has worked on.
- **Average monthly hours**: Average hours worked per month.
- **Tenure**: Length of time (years) an employee has been with the company.
- **Work accidents**: Records of workplace accidents.
- **Promotion in last 5 years**: Whether the employee received a promotion within the last 5 years.
- **Department**: The functional department of the employee (e.g., Sales, HR).
- **Salary**: Categorical variable indicating salary level (Low, Medium, High).
- **Retention**: The target variable indicating whether an employee left the company (Yes/No).

## Methodology

### 1. Data Cleaning and Preprocessing
- Addressed missing values and handled duplicate records to ensure dataset integrity.
- Encoded categorical features such as **department** and **salary** using one-hot encoding for compatibility with machine learning models.
- Identified and removed outliers in the **tenure** column to improve model accuracy and stability.

### 2. Exploratory Data Analysis (EDA)
- Conducted univariate and multivariate analysis to understand the distribution of variables.
- Visualized correlations between **job satisfaction**, **monthly hours**, and **promotion** with retention.
- Highlighted patterns such as high attrition among employees with extreme workloads (high or low hours) and low satisfaction scores.

### 3. Model Building and Evaluation
- **Logistic Regression**: A baseline model to assess initial predictive power.
  - Accuracy: 0.82 | AUC: 0.88
- **Decision Tree**: Captures non-linear relationships between features and turnover.
  - Accuracy: 0.97 | AUC: 0.96
- **Random Forest**: Ensemble technique to improve prediction stability.
  - Accuracy: 0.99 | AUC: 0.98
- **XGBoost**: Gradient boosting model known for handling imbalanced data and delivering top-tier performance.
  - Accuracy: 0.99 | AUC: 0.98

### 4. Model Comparison
The best performing models, **Random Forest** and **XGBoost**, both achieved exceptional accuracy and AUC scores, indicating they are well-suited for predicting employee turnover. Feature importance analysis from these models highlighted key factors like **job satisfaction**, **number of projects**, and **promotion history**.

## Results
- **Top Factors Affecting Retention**:
  1. **Job satisfaction**: Low satisfaction is strongly correlated with high turnover.
  2. **Number of projects**: Employees handling more than a manageable number of projects are prone to leaving.
  3. **Promotion**: Lack of promotion in the last 5 years increases turnover risk.
  
- **Model Performance Summary**:
  - **Random Forest** and **XGBoost** models outperformed others, achieving 99% accuracy and an AUC score of 0.98.
  
## Conclusion
The results show that the company can significantly reduce employee turnover by focusing on improving job satisfaction, managing employee workloads, and promoting deserving employees. The models developed are reliable tools for predicting future employee retention based on historical data.

## Recommendations
- **Project Management**: Limit the number of concurrent projects to prevent burnout.
- **Promotion Strategy**: Introduce a more structured promotion timeline, especially for employees with tenure over 4 years.
- **Work-Life Balance**: Encourage regular breaks and reward consistent performance over excessive working hours.
- **Employee Feedback**: Implement continuous feedback loops to monitor and address satisfaction.

