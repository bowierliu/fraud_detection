# Fraud Detection Using Machine Learning

This project demonstrates a comprehensive approach to detecting fraudulent transactions using machine learning models. The pipeline includes data preprocessing, exploratory data analysis, feature engineering, model training, and evaluation. The models used include Logistic Regression, Random Forest, and XGBoost, with a focus on understanding feature importance and optimizing prediction performance.

---

## Table of Contents
- [Introduction](#introduction)
- [Data Description](#data-description)
- [Approach](#approach)
- [Models and Performance](#models-and-performance)
- [Key Insights](#key-insights)
- [Technologies Used](#technologies-used)
- [How to Run](#how-to-run)
- [Results](#results)

---

## Introduction
Fraudulent transactions pose significant challenges in the financial industry. This project aims to leverage machine learning to detect potential fraud using structured datasets, focusing on improving classification accuracy and interpretability.

---

## Data Description
The project uses a combination of datasets related to transactions, customer profiles, and merchant information. Key datasets include:

- **Customer Profiles:** Contains customer demographic and account information.
- **Transaction Data:** Includes details about transactions, such as amounts, timestamps, and categories.
- **Fraud Indicators:** Labels indicating whether a transaction is fraudulent.
- **Anomaly Scores:** Numerical values representing anomaly likelihood.
- **Merchant Data:** Information about merchants involved in transactions.

Each dataset was loaded, merged, and preprocessed to create a unified dataset for analysis and modeling.

---

## Approach
1. **Data Preprocessing:**
   - Missing value imputation.
   - Encoding categorical variables.
   - Feature scaling with MinMaxScaler.
   - Removal of high-missing-value columns and leakage-prone features.

2. **Exploratory Data Analysis (EDA):**
   - Distribution of the target variable (`FraudIndicator`).
   - Correlation heatmap for numerical features.
   - Box plots to detect outliers.

3. **Modeling:**
   - Logistic Regression.
   - Random Forest.
   - XGBoost.

4. **Evaluation Metrics:**
   - Classification Report (Precision, Recall, F1-Score).
   - ROC-AUC Score.
   - Confusion Matrix.

5. **Feature Importance:**
   - Analyzed feature contributions using XGBoost.

---

## Models and Performance
### Logistic Regression
- **Accuracy:** 54%
- **ROC-AUC:** 0.62
- Struggles to distinguish between fraudulent and non-fraudulent transactions.

### Random Forest
- **Accuracy:** 95%
- **ROC-AUC:** 0.99
- Excellent performance with minimal misclassifications.

### XGBoost
- **Accuracy:** 96%
- **ROC-AUC:** 0.99
- Best-performing model, with high precision, recall, and F1-scores.

---

## Key Insights
- **Top Features:** Transaction `Category`, `CustomerID`, `TimeGap`, and `AnomalyScore` are critical for fraud detection.
- XGBoost and Random Forest outperform Logistic Regression, showcasing the importance of ensemble methods for complex datasets.
- Feature importance analysis highlights areas for data preprocessing and further exploration.

---

## Technologies Used
- **Programming Language:** Python
- **Libraries:**
  - Data Processing: `pandas`, `numpy`
  - Visualization: `matplotlib`, `seaborn`
  - Machine Learning: `scikit-learn`, `xgboost`, `imblearn`
  - Model Evaluation: `roc_auc_score`, `classification_report`
