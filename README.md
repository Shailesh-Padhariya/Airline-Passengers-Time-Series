Airline Time Series Forecasting:

Short Description:
This project explores time series forecasting techniques to predict airline passenger trends using Facebook Prophet, ARIMA, and SARIMAX. The goal is to compare model performance and accuracy while identifying seasonality, trends, and stationarity in the dataset.

Project Overview:

Dataset: Monthly airline passenger data

Models Used:
Facebook Prophet – Automated forecasting model for trend and seasonality.
ARIMA (AutoRegressive Integrated Moving Average) – Classical statistical model.
SARIMAX (Seasonal ARIMA with Exogenous Regressors) – Advanced seasonal model.
Auto ARIMA – Automatically selects the best ARIMA parameters.

Objective: Predict future passenger numbers and compare forecasting techniques.

Time Series Analysis:

Stationarity Check (Augmented Dickey-Fuller Test)

Before Differencing (Non-Stationary Data)
Test Statistic: 0.815
P-value: 0.991 (Fail to reject null hypothesis; data is non-stationary)

After Differencing (Stationary Data):
Test Statistic: -5.098
P-value: 0.000014 (Reject null hypothesis; data is now stationary)

Best ARIMA Model (Auto ARIMA Selection)
Optimal Model: ARIMA(2,1,1)(0,1,0)[12]
The model was chosen based on AIC/BIC minimization criteria.

Model Performance & Evaluation:

1. Facebook Prophet Results
Mean Absolute Error (MAE): 17.38
Mean Squared Error (MSE): 505.26
Root Mean Squared Error (RMSE): 22.48
Mean Absolute Percentage Error (MAPE): 7.27%
R² Score: 0.9646

ARIMA/SARIMAX Model Results
Best Auto ARIMA Model: ARIMA(2,1,1)(0,1,0)[12]
R² Score: 0.9891 (Higher than Prophet, indicating a better fit)

Features & Insights

Trend & Seasonality Detection – Identifies underlying patterns in airline passenger demand.
Model Comparison – Evaluates statistical (ARIMA/SARIMAX) vs. machine learning-based (Prophet) forecasting.
Residual Analysis – Ensures models meet assumptions for reliable predictions.
Performance Metrics – Uses MAE, MSE, RMSE, MAPE, and R² for accuracy comparison.

Tools & Techniques Used:

Time Series Forecasting Models: Facebook Prophet, ARIMA, SARIMAX, Auto ARIMA.
Statistical Analysis: Augmented Dickey-Fuller Test for stationarity check.

Libraries Used:
pandas, numpy – Data preprocessing and manipulation.
matplotlib, seaborn – Data visualization.
statsmodels – ARIMA and stationarity tests.
fbprophet – Facebook Prophet implementation.
pmdarima – Auto ARIMA model selection.

Use Case:

This project is valuable for:
Airline companies optimizing flight schedules and resource allocation.
Business analysts forecasting demand trends for strategic decision-making.
Data scientists comparing traditional statistical and machine learning forecasting techniques.

How to Use
Load the dataset and preprocess it for analysis.
Perform stationarity checks and transformations.
Train Prophet, ARIMA, and SARIMAX models on historical data.
Compare forecast accuracy using RMSE, MAPE, and R² scores.
Use the best model for future airline passenger demand predictions.
