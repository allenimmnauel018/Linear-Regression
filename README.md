# Linear Regression on Housing Dataset

**Source:** Task-3.ipynb

## Overview

This project uses multiple linear regression to predict house prices from the `Housing.csv` dataset. The workflow includes data loading, feature engineering, outlier removal, encoding, scaling, correlation analysis, model training, evaluation, and visualization.

## Steps Performed

### 1. Data Loading

* Loaded the dataset `Housing.csv` using **pandas**.

### 2. Feature Engineering

* **`area_per_room`**: Calculated as `area / (bedrooms + bathrooms)`, handling division by zero.
* **`area_squared`**: Square of the `area` column to capture non-linear effects.

### 3. Outlier Removal

* Used **Interquartile Range (IQR)** to remove outliers in the `price` column:
  - Calculated Q1 (25th percentile) and Q3 (75th percentile).
  - Computed IQR = Q3 - Q1.
  - Kept rows where `price` is within `[Q1 - 1.5*IQR, Q3 + 1.5*IQR]`.

### 4. Encoding

* Converted categorical variables into dummy variables using `pd.get_dummies()` with `drop_first=True`.

### 5. Correlation Analysis

* Created a heatmap using **Seaborn** to visualize correlations between features and the target (`price`).

### 6. Train/Test Split & Scaling

* Split data into **80% training** and **20% testing** sets using `train_test_split`.
* Standardized features **after splitting** using `StandardScaler` from `sklearn.preprocessing` to avoid data leakage.

### 7. Model Training & Evaluation

* Trained a **Linear Regression** model using `sklearn.linear_model.LinearRegression`.
* Evaluated model performance using:
  - **Mean Squared Error (MSE)**
  - **R² Score**
* Visualized **Actual vs Predicted Prices** with a scatter plot.

## Results

* **Mean Squared Error (MSE):** Printed in console during execution.
* **R² Score:** Printed in console during execution.

## Visualization

1. **Heatmap** of feature correlations.
2. **Actual vs Predicted** scatter plot with a reference line.

## Technologies Used

* **Python**
* **pandas** (Data handling)
* **matplotlib, seaborn** (Visualization)
* **scikit-learn** (Preprocessing, Modeling, Evaluation)

## How to Run

1. Place `Housing.csv` in the same directory as `Task-3.ipynb`.
2. Run all cells in the notebook.
3. Review the printed metrics and generated plots.

---

## Author

Jenish Allen Immanuel 💙