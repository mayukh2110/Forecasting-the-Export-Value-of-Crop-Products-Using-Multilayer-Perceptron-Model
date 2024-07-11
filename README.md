# Multilayer Perceptron Model for Forecasting Crop Export Values

This repository contains a detailed report on using a Multilayer Perceptron (MLP) model to forecast the export values of crop products. The report covers the model's performance evaluation, architecture, feature selection, preprocessing steps, and results. 

## Model Performance

The model's performance is evaluated using Mean Squared Error (MSE) and R-squared (R²) metrics. 

- **Mean Squared Error (MSE)**:
  - Validation Set: 0.00546
  - Test Set: 0.0764
- **R-squared (R²)**:
  - Validation Set: 0.9945
  - Test Set: 0.9237

These metrics indicate the model's high accuracy in predicting export values, with an R² value of 0.9945 on the validation set and 0.9237 on the test set.

## Model Architecture

The MLP model consists of three dense layers with 100, 50, and 1 units respectively. Dropout layers are included to prevent overfitting.

- **Layer 1**: Dense (100 units) + Dropout
- **Layer 2**: Dense (50 units) + Dropout
- **Layer 3**: Dense (1 unit)

## Preventing Overfitting

To prevent overfitting, the model incorporates:
1. **Dropout Regularization**
2. **Early Stopping**
3. **Reduce Learning Rate on Plateau**

## Features and Labels

A total of 19 features were selected to capture various dimensions influencing crop export values:

- Year
- Area
- Months
- Value
- Average Annual Inflation
- Inflation Volatility
- Average Temperature Change
- Average Production Value
- Total Production Value
- Total Food Security Index
- Average Emissions
- Total Emissions
- Total Employment
- Total Exchange Rate
- Total Fertilizers Use
- Total Food Balances
- Total FDI
- Total Land Use
- Total Pesticides Use

The primary target variable (label) is the export value (USD) of crop products.

## Preprocessing Steps

1. **Handling Missing Values**:
   - Numerical features: Replaced with the mean
   - Categorical features: Replaced with the mode

2. **Feature Scaling**:
   - StandardScaler: Used to standardize features to have a mean of 0 and a standard deviation of 1

3. **Encoding Categorical Variables**:
   - One-hot encoding: Converts categorical variables into a binary format

4. **Train-Test Split**:
   - The data is split into training and testing sets using an 80-20 ratio.

## Results

The report provides a detailed breakdown of the first ten predictions along with their actual values, illustrating the model's accuracy and robustness.

## Conclusion

The MLP model demonstrates exceptional performance in forecasting crop export values, explaining approximately 99.45% of the variance in the validation set and 92.37% in the test set. This model can serve as a valuable tool for agricultural trade forecasting and decision-making.

---

**Keywords**: Machine Learning, Multilayer Perceptron, Crop Export Forecasting, Regression, Model Evaluation, Preprocessing, Feature Engineering

---
