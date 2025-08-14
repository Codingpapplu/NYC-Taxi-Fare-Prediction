# 🚕 NYC Taxi Fare Prediction - Multiple Linear Regression

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-1.3+-green.svg)](https://pandas.pydata.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📊 Project Overview

**Business Problem**: The NYC Taxi & Limousine Commission needed a reliable method to predict taxi fares before rides begin, enabling transparent pricing for customers and improved operational efficiency.

**Solution**: Developed a multiple linear regression model achieving 88.3% accuracy in fare prediction with an average error of only $2.19.

## 🎯 Key Results

| Metric | Training | Testing |
|--------|----------|---------|
| **R² Score** | 0.869 | 0.883 |
| **MAE** | $2.21 | $2.19 |
| **RMSE** | $3.82 | $3.57 |

**Business Impact**: Model enables pre-trip fare estimates within ±$2.19, suitable for customer-facing applications.

## 🛠️ Technical Implementation

### Data Processing
- **Dataset**: 22,699 NYC taxi trips (2017)
- **Feature Engineering**: Created route-based aggregations (mean_distance, mean_duration)
- **Outlier Treatment**: IQR-based capping for fare amounts and trip durations
- **Categorical Encoding**: One-hot encoding for vendor, rate codes, payment types

### Model Architecture
- **Algorithm**: Multiple Linear Regression with StandardScaler normalization
- **Features**: 30 engineered features including temporal, route, and categorical variables
- **Cross-validation**: 80/20 train-test split with random_state=0

### Key Findings
1. **Top Predictors**: `mean_distance` (coef: 5.85) and `mean_duration` (coef: 3.36)
2. **Rate Code Effects**: JFK airport trips show significant fare premiums
3. **Temporal Patterns**: Minimal rush hour impact on base fares
4. **Model Assumptions**: Residuals show normal distribution and homoscedasticity

## 📁 Repository Structure

