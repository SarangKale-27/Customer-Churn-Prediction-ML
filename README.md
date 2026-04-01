# Customer Churn Prediction

## Project Overview
This project predicts whether a telecom customer is likely to churn (leave the service).  
The goal is to help businesses identify at-risk customers early and take retention actions.

## Problem Statement
Customer churn directly impacts revenue.  
By building a machine learning model, we can predict churn probability and support data-driven customer retention strategies.

## Dataset
- **Domain:** Telecom customer data
- **Target Variable:** `Churn Value` / `Churn Label`
- **Key Features:** Tenure, Monthly Charges, Total Charges, Contract Type, Internet Service, Payment Method, etc.

## Workflow
1. Data loading and basic inspection  
2. Data cleaning (missing values, dropping irrelevant columns)  
3. Exploratory Data Analysis (EDA)  
4. Feature encoding (`pd.get_dummies`)  
5. Train-test split (stratified)  
6. Model training (Random Forest Classifier)  
7. Model evaluation (Accuracy, ROC-AUC, Classification Report, Confusion Matrix)  
8. Feature importance analysis  

## Model Used
- **RandomForestClassifier**
  - `n_estimators=200`
  - `max_depth=10`
  - `class_weight='balanced'`
  - `random_state=42`

## Results
- **Accuracy:** `0.771`
- **ROC-AUC:** `0.851`
- Model shows good discrimination ability for churn prediction.

## Key Business Insights
1. **Tenure Months** is one of the strongest churn indicators.  
2. **Total Charges** and **Monthly Charges** significantly influence churn behavior.  
3. **Contract type** (especially long-term contracts) strongly affects customer retention.

## Conclusion
The model performs well for churn prediction and can be used as a decision-support tool for retention campaigns.  
With further tuning and validation, this can be improved for production-level use.

## Future Improvements
- Hyperparameter tuning (GridSearchCV / RandomizedSearchCV)
- Cross-validation for robust model validation
- Compare with XGBoost / LightGBM
- Deploy as a Streamlit/Flask app for real-time predictions

## How to Run
1. Install dependencies:
   ```bash
   pip install -r requirements.txt

