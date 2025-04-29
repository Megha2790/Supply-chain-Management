# 📄 Final Report
# Title: Product Sales Classification and Demand Forecasting for Supply Chain Management

## 1. Introduction
- In today's competitive market, effective supply chain management requires both the ability to classify products based on sales performance and to accurately forecast future demand. This project aims to apply machine learning techniques to achieve two objectives:
- Classify products into high-selling and low-selling categories.
- Forecast the number of products sold using regression modeling.

## 2. Data Overview
- Dataset: A supply chain dataset with 100 product entries.
- Features: Included pricing, availability, stock levels, order quantities, lead times, manufacturing and shipping details, etc.- 
- Target Variables:
- Classification Target: High seller (1) or Low seller (0).
- Forecasting Target: Number of products sold (continuous).

## 3. Methodology

### 3.1 Data Preprocessing
- Dropped irrelevant and leakage-prone columns such as SKU, Customer demographics, and Inspection results.
- Categorical features were one-hot encoded.
- Numerical features were standardized where necessary.
- Data was split into training and testing subsets (80% training, 20% testing).

## 3.2 Classification Model
- Algorithm: LightGBM Classifier (LGBMClassifier)
- Goal: Classify products into high or low sellers.
- Evaluation Metrics: Precision, Recall, F1-Score, Accuracy.
*  Results:
- Accuracy: 100%
- Precision, Recall, F1-Score: 1.00 across both classes.
- Insights: The model perfectly classified all products without any misclassifications.

## 3.3 Demand Forecasting Model
- Algorithms Tested:
- LightGBM Regressor (LGBMRegressor)
- Linear Regression
- Features Selected:
  Price, Availability, Stock Levels, Lead Times, Order Quantities, Shipping Costs, Production Volumes, Manufacturing Costs, Defect Rates, Costs.
* Evaluation Metrics:
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score (Coefficient of Determination)
* Results:
- LightGBM Regressor:
- MAE: 312.98
- RMSE: 366.39
- R² Score: -0.41
* Linear Regression:
- MAE: 341.67
- RMSE: 388.78
- R² Score: -0.58
* Insights:
- Both regression models exhibited high error rates and negative R² scores, indicating poor predictive performance.
- The primary cause for low performance is the small dataset size and lack of critical external factors such as promotions, seasonality, or market trends.

## 4. Challenges and Limitations
- Small Dataset: Only 100 samples, insufficient for training high-performing machine learning models.
- Missing External Features: Factors like marketing efforts, seasonality, competitor pricing, etc., were not included.
- Possible Noisy Relationships: Features included may not have a strong direct correlation with product sales quantity.

## 5. Recommendations
- Expand Dataset: Collect more historical data and include external influencing factors.
- Feature Engineering: Create new variables (e.g., revenue per unit, stock turnover ratio).
- Modeling Enhancements: Experiment with ensemble methods, time series forecasting, and domain-specific modeling.
- Periodic Retraining: Regularly retrain models with updated datasets to capture evolving demand patterns.

## 6. Conclusion
This project successfully classified products into high and low sellers with perfect accuracy using the LightGBM Classifier. Although demand forecasting models did not achieve high predictive performance due to dataset limitations, the exercise provided valuable insights into the data characteristics and modeling approaches suitable for supply chain analytics.

Future improvements, especially in data richness and volume, are critical to achieving better forecasting accuracy and driving smarter supply chain decisions.

## ✅ End of Report
