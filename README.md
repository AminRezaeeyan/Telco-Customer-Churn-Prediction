# Telco Customer Churn Prediction

This project aims to predict customer churn for a telecommunications company using machine learning techniques. The dataset includes customer information such as demographics, account information, services, and usage patterns, with the goal of predicting whether a customer will churn (leave the company).

## Project Overview

Customer churn is a critical issue for businesses, especially in industries with high competition like telecommunications. By identifying customers who are likely to churn, companies can take proactive measures to retain them, such as offering discounts or improving customer service.

In this project, we utilize **LightGBM**, a powerful gradient boosting algorithm, along with data preprocessing, exploratory data analysis (EDA), feature engineering, and model evaluation techniques to predict customer churn.

## Dataset

The dataset used in this project is publicly available on [Kaggle - Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn). The dataset consists of the following columns:

- **customerID**: Unique identifier for each customer.
- **gender**: Gender of the customer (Male/Female).
- **SeniorCitizen**: Whether the customer is a senior citizen (1: Yes, 0: No).
- **Partner**: Whether the customer has a partner (Yes/No).
- **Dependents**: Whether the customer has dependents (Yes/No).
- **tenure**: Number of months the customer has stayed with the company.
- **PhoneService**: Whether the customer has a phone service (Yes/No).
- **MultipleLines**: Whether the customer has multiple phone lines (Yes/No/No phone service).
- **InternetService**: Type of internet service (DSL, Fiber optic, No).
- **OnlineSecurity**: Whether the customer has online security service (Yes/No/No internet service).
- **OnlineBackup**: Whether the customer has an online backup service (Yes/No/No internet service).
- **DeviceProtection**: Whether the customer has device protection (Yes/No/No internet service).
- **TechSupport**: Whether the customer has tech support service (Yes/No/No internet service).
- **StreamingTV**: Whether the customer has a streaming TV service (Yes/No/No internet service).
- **StreamingMovies**: Whether the customer has a streaming movies service (Yes/No/No internet service).
- **Contract**: The type of contract the customer has (Month-to-month, One year, Two years).
- **PaperlessBilling**: Whether the customer is using paperless billing (Yes/No).
- **PaymentMethod**: The method used for bill payment (Electronic check, Mailed check, Bank transfer, Credit card).
- **MonthlyCharges**: The monthly amount charged to the customer.
- **TotalCharges**: The total amount charged to the customer.
- **Churn**: Target variable indicating if the customer churned (Yes/No).

## Project Workflow

1. **Data Preprocessing**: 
   - Handle missing values, categorical encoding, and outlier detection.
   - Feature scaling using `StandardScaler` for numerical features.

2. **Exploratory Data Analysis (EDA)**: 
   - Perform an analysis of the data distribution, correlations, and visualize trends.
   - Handle imbalanced data using class weighting.
   
3. **Model Training**:
   - Train the model using **LightGBM**, optimized with **Grid Search** for hyperparameter tuning.

4. **Model Evaluation**:
   - Evaluate the model using various metrics such as Accuracy, Precision, Recall, F1-Score, ROC AUC, and Confusion Matrix.
   - Plot ROC curves, confusion matrix, and performance metrics to visualize model performance.

## Results
- **Test Set Results**: 
  - Test Accuracy: 0.7964
  - Test ROC AUC Score: 0.8433

## Key Insights

- The model performed reasonably well in identifying churned customers but has room for improvement, especially in reducing false positives and increasing recall.
- **ROC AUC Score** indicates the model has good discriminatory power.
- Precision and Recall for the churned class (class 1) are moderate, which could be improved by tuning the model or engineering additional features.

## Future Work

- Explore advanced feature engineering techniques, such as time-series analysis for customer behavior or integrating external datasets.
- Implement a model explanation technique like **SHAP** to interpret the model's decisions.

## Contributing
Contributions are welcome! If you'd like to suggest improvements or report issues, please open an issue or submit a pull request.
