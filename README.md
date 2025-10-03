# 🛒 Store Item Demand Forecasting with LightGBM

My Kaggle project on demand forecasting, developed after completing my data science bootcamp.
The goal is to predict the daily sales of various store–item combinations using time series forecasting techniques.

---

## 📊 Results

- Validation SMAPE: 13.53
- Training SMAPE: 12.76
- Algorithm: LightGBM Regressor
- Evaluation Metric: SMAPE (Symmetric Mean Absolute Percentage Error)

---

## 🚀 Project Overview

- This project tackles the Kaggle Store Item Demand Forecasting Challenge.
- It focuses on time series feature engineering combined with gradient boosting methods to generate accurate forecasts.

**Key Features:**

- Advanced time series feature engineering (lag, rolling, exponentially weighted mean features)
- Log transformation of the target variable for variance stabilization
- Custom evaluation metric (SMAPE)
- Time-based train/validation split (respecting temporal order)
- Feature importance analysis for interpretability

---

## 📈 Methodology

**Data Exploration & Cleaning**

- Combined train/test sets for consistent preprocessing
- Handled missing values
- Checked store & item distributions
- Feature Engineering
- Date-based features: month, day, week, year, weekday, weekend, month start/end
- Lag features: 91, 98, 105, 112, 182, 364, 546, 728 days
- Rolling mean features: 365, 546 days
- Exponentially Weighted Means (EWM): various alpha values & lags
- One-hot encoding for categorical features (store, item, month, weekday)
- Target transformation with log1p(sales)

---

**Model Training**

- LightGBM Regressor with tuned parameters
- Custom SMAPE metric for evaluation
- Early stopping to prevent overfitting
- Evaluation
- Validation period: 2017 Q1
- Training on data before 2017
- SMAPE used as main metric

---

## 🎯 Key Learnings

- Time-based features (lags, rolling stats, EWM) dramatically improve forecast accuracy
- Log-transforming target stabilizes variance and improves model performance
- Time-aware validation (avoiding data leakage) is critical in demand forecasting
- Even with gradient boosting, proper feature engineering is the most impactful step

---

## 🔗 Links

Kaggle Competition: [Store Item Demand Forecasting Challenge](https://www.kaggle.com/competitions/demand-forecasting-kernels-only)
Kaggle Notebook: [My Solution](https://www.kaggle.com/code/oxspaceman/store-item-demand-forecasting)

--- 

## 📝 About

This project represents one of my first time series forecasting challenges tackled after my data science bootcamp.
It showcases how classical ML (LightGBM) can effectively compete in forecasting tasks when combined with careful feature engineering.

- Status: Completed ✅
- Validation SMAPE: 13.53
- Training SMAPE: 12.76
