# House Price Prediction (Regression)

## Introduction to Artificial Intelligence - Group 4 Assignment


## Project Overview
- **Problem Type**: Regression (continuous value prediction)
- **Dataset**: California Housing Prices
- **Target Variable**: `median_house_value`
- **Goal**: Build and compare machine learning models to predict house prices based on various features such as location, income, and housing characteristics.

---

## Dataset Description
The project uses the **California Housing Prices** dataset.
- **Total Entries**: 20,640
- **Features**:
    - `longitude`, `latitude`: Geographical location.
    - `housing_median_age`: Median age of houses in the block.
    - `total_rooms`, `total_bedrooms`: Count of rooms and bedrooms.
    - `population`, `households`: Population and household counts.
    - `median_income`: Median income of residents.
    - `ocean_proximity`: Categorical location relative to the ocean.

---

## Data Preprocessing
The project implements a robust preprocessing pipeline using Scikit-Learn's `Pipeline` and `ColumnTransformer`:
- **Numeric Features**:
    - Missing values handled using `SimpleImputer` (strategy: median).
    - Data scaling using `StandardScaler`.
- **Categorical Features**:
    - Missing values handled using `SimpleImputer` (strategy: most frequent).
    - Encoding using `OneHotEncoder` (handling unknown categories by ignoring them).

---

## Model Performance Ranking
The following models were trained and evaluated on the test set, ranked by their **R2 Score**:

1. **KNN (k=7)**
   - **R2 Score**: 0.731615
   - **MAE**: $40,337.91
   - **MSE**: 3.549e+09
2. **Decision Tree (max_depth=15)**
   - **R2 Score**: 0.677310
   - **MAE**: $41,197.10
   - **MSE**: 4.267e+09
3. **Linear Regression**
   - **R2 Score**: 0.663452
   - **MAE**: $49,016.60
   - **MSE**: 4.450e+09

---

## Key Insights & Conclusion
- **Best Model**: **KNN (k=7)** outperformed the other models, explaining approximately **73.16%** of the variance in house prices.
- **Performance Gap**: There is a notable performance difference (approx. 6.82% in R2) between the best model (KNN) and the baseline Linear Regression.
- **Recommendations**: The KNN model shows strong predictive power and can be reliably used for house price predictions in this context. Future improvements could involve ensemble methods or further hyperparameter tuning.
