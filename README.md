# module20
Capstone Submission Module 20-1

# California Housing Price Prediction: Capstone Project

## 📘 Overview
This project investigates the research question:  
**“How do socio-economic and geographic factors influence housing prices in California, and can machine learning models accurately predict housing prices based on these features?”**  

The goal is to perform exploratory data analysis (EDA), clean and engineer features, and build a baseline machine learning model to predict housing prices. Insights from this work will inform future iterations with more advanced models and optimizations.  

---

## 🎯 Objectives
- Perform EDA to understand patterns and relationships in the data.  
- Clean and preprocess the dataset to prepare it for modeling.  
- Engineer relevant features to enhance model performance.  
- Develop and evaluate a baseline machine learning model.  
- Analyze results and identify next steps for improvement.  

---

## 📊 Data Cleaning and EDA

### ✅ Steps Taken:
1. **Handle Missing Values:**
   - Total missing values: `207` in `total_bedrooms`
   - Action: Removed rows with missing values.
   - Shape reduced from **(20,640, 10)** to **(20,433, 10)**.

2. **Remove Duplicates:**
   - No duplicates found. Shape unchanged: **(20,433, 10)**.

3. **Outlier Detection and Removal:**
   - Used the **IQR method** to identify outliers in numeric columns.
   - Shape reduced from **(20,433, 10)** to **(17,434, 10)**.

4. **Feature Engineering:**
   - Encoded `ocean_proximity` using one-hot encoding.  
   - Created new features:  
     - `rooms_per_household`
     - `rooms_that_are_bedrooms`
     - `population_per_household`  
   - Final dataset shape: **(17,434, 16)**  

---

## 🤖 Baseline Model: Linear Regression

### 📁 Modeling Steps
1. **Data Split:**
   - Train/Test split: 80% / 20%  
   - X_train shape: **(13,947, 15)**  
   - X_test shape: **(3,487, 15)**  

2. **Train Baseline Model:**
   - Used **Linear Regression** from `sklearn`.  

3. **Model Evaluation:**
   - **Mean Squared Error (MSE):** 3,213,623,454.58  
   - **Root Mean Squared Error (RMSE):** $56,688.83  
   - **R-squared (R²):** 0.6311  

4. **Feature Importance:**
   - Top influencing features:  
     - `rooms_that_are_bedrooms`
     - `ocean_proximity_ISLAND`
     - `median_income`
     - `longitude`, `latitude`

---

## 📌 Key Insights
- The Linear Regression baseline explains **63.1%** of the variance in housing prices.  
- Average prediction error (RMSE) of ~$56K highlights room for improvement.  
- **Socio-economic (median income)** and **geographic factors (latitude, longitude, ocean proximity)** are strong predictors of housing prices.  

---

## 🚀 Potential Next Steps
- Explore advanced models: **Random Forest, Gradient Boosting, or XGBoost**.  
- Perform hyperparameter tuning to improve accuracy.  
- Investigate feature interactions and non-linear relationships.  
- Visualize geographic trends using heatmaps.  

