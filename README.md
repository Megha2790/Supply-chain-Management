# Supply Chain Management - Demand Forecasting Report
## 1. Overview
Objective: To forecast the number of products sold using a machine learning model.

Model Performance:

Mean Absolute Error (MAE): Low, showing high accuracy.

R² Score: High (close to 1), indicating an excellent fit.

## 2. Data Preprocessing
Missing values were evaluated and addressed appropriately.

Redundant or irrelevant columns (SKU, Customer demographics, Inspection results) were dropped to avoid data leakage.

Features were categorized into numerical and categorical variables.

Categorical variables were handled using One-Hot Encoding.

Data was split into training and testing sets for model evaluation.

## 3. Model Building
A LightGBM Regressor model (LGBMRegressor) was used to predict the number of products sold.

A preprocessing pipeline was created for cleaner handling of different feature types.

The model was trained and validated effectively, ensuring robustness and speed.

## 4. Model Evaluation
The model achieved:

Low MAE, meaning predictions were close to the true values.

High R² Score, meaning the model explained a large proportion of variance.

Business Insights:

All high-selling and low-selling products were correctly predicted without misclassification.

This indicates excellent model accuracy and high confidence for operational use.

## 5. Model Deployment
While the model saving process (serialization) was not explicitly shown, it can be easily saved for production use via joblib or pickle.

The model outputs are ready to be integrated into supply chain decision-making systems to drive better inventory management, marketing focus, and production planning.

## Conclusion
The LightGBM model delivers highly accurate forecasts of product sales, enabling significant improvements in inventory management, reduction in stockouts, and better alignment of supply chain strategies. Regular model retraining with updated data will help maintain its predictive performance over time.
