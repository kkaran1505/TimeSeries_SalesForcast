# TimeSeries_SalesForcast
Sales Forecasting for Retail Stores

Project Overview

This project aims to predict daily sales for each product family at each store for the next 15 days using various forecasting models. The dataset includes historical sales data, store information, oil prices, and holiday events. The goal is to build an accurate forecasting model to assist in inventory planning and business decision-making.

Data Sources

train.csv: Historical sales data for different product families across multiple stores.

stores.csv: Store metadata including store type and cluster.

oil.csv: Daily oil price data, which may influence sales trends.

holidays_events.csv: Calendar of holidays, promotions, and special events.

Project Workflow

1: Data Preparation

I.Data Cleaning

Handle missing values (e.g., interpolate missing oil prices).

Convert date columns to datetime format.

Merge external datasets (stores, oil prices, holidays) with sales data.

II.Feature Engineering

Time-based Features: Extract day, week, month, year, and weekday.

Event-based Features: Create flags for holidays, promotions, paydays, and other significant events.

Rolling Statistics: Compute moving averages, rolling standard deviations, and lagged features.

Store-Specific Aggregations: Identify top-performing product families per store cluster.

III.Exploratory Data Analysis (EDA)

Visualize sales trends over time.

Analyze the impact of holidays and promotions.

Check correlations between oil prices and sales.

Identify anomalies in the data.

2: Model Selection & Forecasting

Baseline Model

Naïve Forecasting for comparison.

Advanced Models

ARIMA (AutoRegressive Integrated Moving Average)

Random Forest Regressor

XGBoost / LightGBM

LSTM (Long Short-Term Memory Neural Network)

Prophet Model (for capturing seasonality)

I.Model Evaluation

RMSE (Root Mean Square Error)

MAPE (Mean Absolute Percentage Error)

R² Score

II.Visual Comparison of historical vs. predicted sales

Visualization & Insights

Historical vs. Forecasted Sales Plots.

Feature Importance Analysis.

Business insights for inventory management and promotional strategies.

Installation & Requirements

To run this project, install the following dependencies:

pip install pandas numpy matplotlib seaborn scikit-learn xgboost lightgbm tensorflow statsmodels prophet

This script cleans the dataset, handles missing values, merges external data sources, and generates additional features.

Train the forecasting models:

This script trains multiple models, evaluates their performance, and saves the best model for forecasting.

This script loads the best-performing model and makes sales predictions for the next 15 days.

Visualize the results:

This script generates plots comparing historical vs. predicted sales and highlights key trends.

Results & Business Impact

The best-performing model is selected based on RMSE.

Provides insights for optimizing stock levels and planning promotions.

Helps in decision-making for better demand forecasting.
