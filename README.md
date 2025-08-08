# Linear Regression on Housing Dataset

**Source:** Task-3.ipynb

## Overview

This project implements a **Multiple Linear Regression** model to predict **house prices** based on various features from the `Housing.csv` dataset. It includes data preprocessing, feature engineering, outlier handling, scaling, model training, evaluation, and visualization.

## Steps Performed

### 1. Data Loading

* The dataset `Housing.csv` was loaded using **pandas**.

### 2. Feature Engineering

* **`area_per_room`**: Calculated as `area / (bedrooms + bathrooms)`, avoiding division by zero.
* **`area_squared`**: Square of the `area` column to capture non-linear effects.

### 3. Outlier Removal

* Used **Interquartile Range (IQR)** to remove outliers in the `price` column:

  ```
  Q1 = 25th percentile
  Q3 = 75th percentile
  IQR = Q3 - Q1
  price kept within [Q1 - 1.5*IQR, Q3 + 1.5*IQR]
  ```

### 4. Encoding & Scaling

* Converted categorical variables into dummy variables with `pd.get_dummies()` and `drop_first=True` to avoid multicollinearity.
* Standardized features using **StandardScaler** from `sklearn.preprocessing`.

### 5. Correlation Analysis

* Created a heatmap using **Seaborn** to visualize correlations between features and the target (`price`).

### 6. Model Training

* Split data into **80% training** and **20% testing** sets.
* Trained a **Linear Regression** model using `sklearn.linear_model.LinearRegression`.

### 7. Model Evaluation

* **Metrics Used:**

  * **Mean Squared Error (MSE)**: Measures average squared difference between predicted and actual values.
  * **R² Score**: Proportion of variance explained by the model.
* Visualized **Actual vs Predicted Prices** with a scatter plot.

## Results

* **Mean Squared Error (MSE):** Printed in console during execution.
* **R² Score:** Printed in console during execution.

## Visualization

1. **Heatmap** of feature correlations.
2. **Actual vs Predicted** scatter plot with a reference line.

## Technologies Used

* **Python**
* **Pandas, NumPy** (Data handling)
* **Matplotlib, Seaborn** (Visualization)
* **Scikit-learn** (Preprocessing, Modeling, Evaluation)

## How to Run

1. Place `Housing.csv` in the same directory as `Task-3.ipynb`.
2. Run all cells in the notebook.
3. Check printed metrics and plots.

---

## 👨‍💻 Author

Jenish Allen Immanuel J
