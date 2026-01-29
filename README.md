# Absa_Customer_income_predictions

Absa Customer Income Prediction
📌 Project Overview

This project focuses on predicting a customer’s declared net income using their transaction history and demographic information.
The dataset comes from the Absa Customer Income Prediction Challenge on Zindi, where the goal is to build a machine learning model that can estimate income based on customer behavior over 14 months.

🎯 Problem Statement

Banks collect large amounts of transaction data, but income is not always directly available.
The objective of this project is to use machine learning to predict customer income from:

Transaction patterns

Demographic details

Employment information

This helps banks better understand customers for credit scoring, risk analysis, and product recommendations.

📂 Dataset Description

The project uses multiple datasets:

Train.csv – Customer IDs with declared net income (target variable)

Test.csv – Customer IDs without income (used for prediction)

Transactions.csv – 14 months of transaction history per customer

Customer.csv – Demographic information

Employment_status.csv – Employment categories

Income_group.csv – Income grouping descriptions

SampleSubmission.csv – Submission format

🛠 Data Preparation & Feature Engineering

Raw transaction data is too detailed for direct modeling, so it is summarized per customer.

Key steps:

Handle missing values using median or mode

Aggregate transaction data to create features such as:

Total transaction amount

Average transaction amount

Number of transactions

Maximum and minimum transaction values

Encode categorical variables (e.g. employment status)

Merge transaction features with demographic data

🤖 Model Used
Random Forest Regression

Random Forest Regression was chosen because:

It handles non-linear relationships

It works well with mixed data types

It is robust to noise and outliers

It provides feature importance, improving interpretability

Important hyperparameters:

n_estimators – Number of trees in the forest

max_depth – Limits tree complexity to prevent overfitting

min_samples_leaf – Ensures stable predictions by avoiding very small splits

📊 Model Evaluation

The training data is split into training and validation sets

Performance is measured using regression error metrics (e.g. MAE / RMSE)

Feature importance is analyzed to understand what drives income prediction

📈 Results

The model successfully learns patterns from customer transaction behavior and demographics to predict income.
Key predictors include:

Total transaction amount

Average transaction value

Number of transactions

Employment status

Age

🚀 Future Improvements

Incorporate time-based trends (monthly spending behavior)

Try advanced models such as Gradient Boosting (XGBoost, LightGBM)

Perform deeper hyperparameter tuning

Add customer segmentation (clustering)

🧠 Key Learnings

Feature engineering is crucial when working with transaction data

Random Forest is a strong baseline for regression problems with complex data

Controlling model complexity helps prevent overfitting

📎 Tools & Libraries

Python

Pandas

NumPy

Scikit-learn

Jupyter Notebook
