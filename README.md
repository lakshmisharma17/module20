# module20

### California Housing Price Prediction: Capstone Project

**Author**
Lakshmi Sharma @lakshmisharma17

#### Executive summary

This project investigates the research question:  
**“How do socio-economic and geographic factors influence housing prices in California, and can machine learning models accurately predict housing prices based on these features?”**  

The goal is to perform exploratory data analysis (EDA), clean and engineer features, and build a baseline machine learning model to predict housing prices. Insights from this work will inform future iterations with more advanced models and optimizations.

#### Rationale

As a resident of California for decades and an  active volunteer in California’s state and city libraries, arts programs, and schools, I have witnessed firsthand the impact of rising housing prices on people’s lives. These increases have affected the overall quality of government spending on essential infrastructure and have had a particularly negative impact on talent pool (young families moving out of state due to unaffordability of housing) and small business owners.

Understanding the socio-economic and geographic factors that influence housing prices is critical for stakeholders such as policymakers, real estate developers, and buyers. A predictive model can help anticipate trends and make data-driven decisions to make targeted investments in infrastructure and retain the talent as well as help small buisness owners in California State in the United States.

#### Research Question

How do socio-economic and geographic factors influence housing prices in California, and can machine learning models accurately predict housing prices based on these features?

#### Data Sources

California housing dataset (20,640 rows, 10 features) sourced from following kaggle repository:
https://www.kaggle.com/datasets/camnugent/california-housing-prices  

#### Methodology

- **Data Cleaning and EDA:**
  - Removed 207 rows with missing values in `total_bedrooms`.
  - Outliers removed using IQR method, reducing dataset to **(17,434, 10)**.
  - Feature engineering: one-hot encoding for `ocean_proximity` and creation of new features (`rooms_per_household`, `rooms_that_are_bedrooms`, `population_per_household`).
  - Final dataset shape: **(17,434, 16)**.

- **Baseline Model:**
  - **Linear Regression** trained with an 80/20 train-test split.
  - **Evaluation metrics:**
    - MSE: 3,213,623,454.58
    - RMSE: $56,688.83
    - R²: 0.6311
  - **Key features:** `rooms_that_are_bedrooms`, `median_income`, `ocean_proximity_ISLAND`, `longitude`, `latitude`

#### Results

- The Linear Regression baseline explains **63.1%** of the variance in housing prices.
- RMSE of ~$56K highlights room for improvement.
- Socio-economic and geographic factors are strong predictors.

#### Next steps

- Explore advanced models (Random Forest and Gradient Boosting).
- Perform hyperparameter tuning to improve accuracy.
- Use pipeline and add scaling 
- (optional) Visualize geographic trends using heatmaps.

#### Outline of project
- Link to the notebook
https://github.com/lakshmisharma17/module20/blob/main/Capstone_Module20_1.ipynb

##### Contact and Further Information
@Lakshmisharma17 (gitHub handle) 
Student of 'Professional Certificate in Machine Learning and Artificial Intelligence', Jan 2025 Cohort

