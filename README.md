## Supplement Sales Prediction

### Project Overview

This project aims to **predict the revenue generated from supplement sales** based on various factors such as product information, units sold, price, discount, location, and platform. The goal is to develop a regression model that can accurately forecast sales revenue, helping supplement businesses optimize pricing strategies, inventory management, and marketing efforts.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - Supplement Sales Data](https://www.kaggle.com/datasets/zahidmughal2343/supplement-sales-data)
  * **Size**: 4384 entries, 10 columns
  * **Key Features**:
      * 'Product Name', 'Category', 'Units Sold', 'Price', 'Discount', 'Units Returned', 'Location', 'Platform'.
  * **Approach**:
      * Data Cleaning: Dropped the 'Date' column as it might be complex to use directly in its current format and simpler features are preferred for initial models. No missing values or duplicates were found.
      * Exploratory Data Analysis: Histograms, Boxplots, and Heatmaps were used for visualization to understand data distributions and correlations.
      * Label Encoding: Applied to all columns, including numerical ones and the target 'Revenue'. *Note: Applying Label Encoding to inherently numerical features like 'Units Sold', 'Price', 'Revenue', 'Discount', 'Units Returned' is not ideal as it imposes an ordinal relationship where none exists. This could potentially affect model performance for a regression task. Ideally, these should be treated as numerical features.*
      * Regression Task: Predicting 'Revenue'.
      * Models Used:
          * Linear Regression, Ridge, XGBoost Regressor, Random Forest Regressor, AdaBoost Regressor, Gradient Boosting Regressor, Bagging Regressor, Decision Tree Regressor, SVR, K-Nearest Neighbors Regressor.
  * **Best R2 Score**:
      * 0.9994 with XGBoost Regressor and Gradient Boosting Regressor.
      * 0.9993 with Random Forest Regressor.
      * 0.9991 with Bagging Regressor.

-----

### Purpose and Applications

  * Enable supplement businesses to **forecast sales revenue** accurately.
  * Optimize pricing and discount strategies for various products.
  * Improve inventory management and reduce stockouts or overstocking.
  * Support data-driven decision-making in marketing campaigns and platform selection.

-----

### Installation

Clone the repository:

```bash
git clone https://github.com/BhaveshBhakta/Supplement-Sales-Prediction-Using-ML.git
cd Supplement-Sales-Prediction-Using-ML
```

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Re-evaluating the preprocessing step of applying Label Encoding to numerical features; consider using standard scaling (e.g., `StandardScaler`) for numerical features and only applying encoding to truly categorical ones.
  * Performing comprehensive hyperparameter tuning and cross-validation for all regression models to maximize predictive performance.
  * Exploring time-series forecasting models if the 'Date' column is re-incorporated and its time-dependent patterns are considered.
  * Adding explainability (e.g., SHAP or LIME) to understand which factors most significantly drive supplement sales revenue.
