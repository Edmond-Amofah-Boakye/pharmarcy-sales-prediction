# Pharmaceutical Sales Forecasting

A comprehensive time series analysis and forecasting project for pharmaceutical sales data, implementing multiple advanced forecasting models to predict drug sales across different categories.

## Project Overview

This project analyzes pharmaceutical sales data from 2014 to 2019, covering various drug categories (M01AB, M01AE, N02BA, N02BE, N05B, N05C, R03, R06). It implements multiple forecasting models to predict future sales trends and provides detailed comparative analysis of model performances.

## Features

- Time series analysis with seasonal decomposition
- Statistical tests for stationarity (Augmented Dickey-Fuller)
- Correlation analysis between different drug categories
- Multiple forecasting models:
  - Random Forest
  - XGBoost
  - ARIMA
  - SARIMA
  - Facebook Prophet
  - Linear Regression
- Comprehensive model evaluation and comparison
- Visual analysis of trends and forecasts

## Installation

1. Clone the repository
2. Install the required dependencies:

```bash
pip install -r requirements.txt
```

Required packages:
- pandas==2.2.0
- numpy
- seaborn
- matplotlib
- scikit-learn
- statsmodels
- pmdarima
- xgboost

## Data Description

The project uses two main datasets:
- `salesweekly.csv`: Weekly sales data
- `salesmonthly.csv`: Monthly sales data

Data features include:
- `datum`: Date of sales
- Drug categories:
  - M01AB: Anti-inflammatory agents
  - M01AE: Anti-inflammatory preparations
  - N02BA: Analgesics
  - N02BE: Anilides
  - N05B: Anxiolytics
  - N05C: Hypnotics and sedatives
  - R03: Anti-asthmatics
  - R06: Antihistamines

## Analysis Features

1. **Data Preprocessing**
   - Date formatting
   - Missing value analysis
   - Duplicate checking
   - Time series indexing

2. **Exploratory Data Analysis**
   - Correlation analysis between drug categories
   - Seasonal pattern identification
   - Trend analysis
   - Sales distribution analysis

3. **Statistical Analysis**
   - Augmented Dickey-Fuller (ADF) test for stationarity
   - ACF and PACF analysis
   - Seasonal decomposition

4. **Model Implementation**
   - Multiple forecasting models with hyperparameter tuning
   - Cross-validation for time series
   - Comprehensive error metrics calculation

## Model Comparison

The project implements and compares several forecasting models:

| Model | Features |
|-------|----------|
| Random Forest | Best overall performance, captures non-linear patterns |
| XGBoost | Gradient boosting implementation |
| ARIMA | Traditional time series forecasting |
| SARIMA | Handles seasonal components |
| Prophet | Robust to missing data and outliers |
| Linear Regression | Baseline model |

## Results

The Random Forest model was selected as the best-performing model based on:
- Consistent prediction accuracy
- Lower Mean Absolute Error (MAE)
- Better capture of seasonal patterns
- Robust performance across different drug categories

## Usage

1. Open and run the Jupyter notebook:
```bash
jupyter notebook src/app.ipynb
```

2. The notebook contains step-by-step analysis:
   - Data loading and preprocessing
   - Exploratory data analysis
   - Model training and evaluation
   - Forecasting and visualization

## Visualizations

The project includes various visualizations:
- Time series plots
- Seasonal decomposition graphs
- Correlation heatmaps
- Forecast vs. Actual comparisons
- Model performance metrics

## Model Selection Justification

The Random Forest model was chosen as the primary forecasting model due to:
1. Consistent performance across different metrics
2. Better handling of non-linear patterns in the data
3. Robust performance with seasonal variations
4. Lower prediction errors compared to other models
5. Better generalization to unseen data

## Project Structure

```
├── README.md
├── requirements.txt
└── src/
    ├── app.ipynb
    ├── salesmonthly.csv
    └── salesweekly.csv
