# Car Price Prediction

This repository contains a Jupyter notebook that demonstrates the process of predicting car prices using various regression models. The analysis includes data exploration, feature engineering, model building, and evaluation.

## Project Overview

The goal of this project is to build and evaluate machine learning models to accurately predict the price of a vehicle based on its various attributes. The process involves several stages, from initial data analysis to comparing the performance of different regression techniques.

## Dataset

The project uses the `CarPrice.csv` dataset, which contains 26 columns and 205 entries. The dataset includes a mix of numerical and categorical features that describe car specifications.

Key features used for prediction include:
- `enginesize`
- `curbweight`
- `horsepower`
- `carwidth`
- `citympg`
- `highwaympg`

The target variable is `price`. The dataset was checked for null values, and none were found.

## Analysis and Modeling

The notebook `CarPricePrediction.ipynb` walks through the complete analysis pipeline.

### 1. Exploratory Data Analysis (EDA)

- **Initial Inspection**: The dataset is loaded, and its basic structure, data types, and summary statistics are examined.
- **Outlier Detection**: Boxplots are used to identify potential outliers in key numerical features like `enginesize`, `curbweight`, and `horsepower`.
- **Feature Distribution**: Histograms are plotted for all numerical features to understand their distributions.
- **Correlation Analysis**: A heatmap is generated to visualize the correlation between numerical variables, helping to identify features strongly related to the `price`. `enginesize`, `curbweight`, `horsepower`, and `carwidth` show strong positive correlations with `price`.

### 2. Simple Linear Regression

A baseline model is created using a single feature, `enginesize`, to predict `price`. The relationship is visualized with a scatter plot and a regression line.

### 3. Multiple Linear Regression

A more complex model is built using multiple features that showed a high correlation with the price: `enginesize`, `curbweight`, and `horsepower`. The model's performance is evaluated using standard metrics.

- **Mean Squared Error (MSE)**: 11,824,364.40
- **Root Mean Squared Error (RMSE)**: 3,438.66
- **R-squared (R²)**: 0.8138

### 4. Polynomial Regression

To capture non-linear relationships between the features and the target variable, a second-degree polynomial regression model is trained on the same set of features (`enginesize`, `curbweight`, `horsepower`).

- **Polynomial MSE**: 10,266,857.33
- **Polynomial RMSE**: 3,204.19
- **Polynomial R²**: 0.8383

The polynomial model shows a modest improvement over the linear model, indicating the presence of non-linear patterns in the data.

### 5. Regularization (Ridge & Lasso)

The notebook also includes implementations of Ridge and Lasso regression, which are techniques used to prevent overfitting in linear models.

### 6. Model Diagnostics

Residual analysis is performed on the multiple linear regression model to check its assumptions. A residual plot (predicted values vs. residuals) is generated to identify any patterns, such as heteroscedasticity.

## Results

The comparison between the models shows that the Polynomial Regression model provides a better fit to the data than the Multiple Linear Regression model.

- **Multiple Linear Regression R²**: 0.814
- **Polynomial Regression R²**: 0.838

This suggests that car prices have a non-linear relationship with features like engine size, curb weight, and horsepower.

## How to Run

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/alokpatel0172-cyber/alok-patel.git
    cd alok-patel
    ```
2.  **Install dependencies:**
    Make sure you have Python and the following libraries installed:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn jupyter
    ```
3.  **Run the notebook:**
    You can run the `CarPricePrediction.ipynb` notebook in a local Jupyter environment or open it directly in Google Colab using the badge provided within the notebook. You will need to upload the `CarPrice.csv` dataset when prompted.
👨‍💻 Contributors
   Pawan Kumar Patel

Alok Patel 
