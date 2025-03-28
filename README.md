# GOOG-Stock-Price-Prediction

## Overview
This project is focused on predicting Google stock prices using time series forecasting methods. We utilize various methods like Simple Moving Average (SMA), Simple Exponential Smoothing (SES), and Holt-Winters Exponential Smoothing to forecast future stock prices based on historical data.

## Dataset
The dataset used in this project is from Kaggle, which contains the historical stock prices of Google from 2016 to 2021. The data includes columns like date, close price, high price, low price, volume, and more.

You can access the dataset from the following link:
[Google Stock Dataset on Kaggle](https://www.kaggle.com/datasets/shreenidhihipparagi/google-stock-prediction)

## Setup

```python
import kagglehub

# Download latest version
path = kagglehub.dataset_download("shreenidhihipparagi/google-stock-prediction")

print("Path to dataset files:", path)

df = pd.read_csv('/root/.cache/kagglehub/datasets/shreenidhihipparagi/google-stock-prediction/versions/2/GOOG.csv')
```

## Methods Used
1. Simple Moving Average (SMA):

- SMA is used with different window sizes (10, 50, 200) to smooth out the fluctuations in stock prices and observe the overall trend.

2. Simple Exponential Smoothing (SES):

- SES is applied with smoothing levels of 0.2 and 0.8 to estimate future stock prices. A lower smoothing value gives more weight to recent data, while a higher smoothing value considers a broader range of data.

3. Holt-Winters Exponential Smoothing:

- This method takes into account both trend and seasonality of stock prices, providing a more accurate forecast by modeling the underlying patterns in the data.

## Key Steps

1. Data Preprocessing:

- The dataset is cleaned and organized, with the "date" column set as the index for time series analysis.

2. Data Decomposition:

- A seasonal decomposition of the stock prices is done to analyze the trend, seasonality, and residuals in the data.

3. Stationarity Test:

- The Augmented Dickey-Fuller (ADF) test is performed to check whether the time series is stationary or not.

4. Modeling:

- We use SMA, SES, and Holt-Winters methods to predict stock prices.

5. Model Evaluation:

- Various performance metrics, such as Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and Mean Absolute Percentage Error (MAPE), are used to evaluate the accuracy of the models.

## Evaluation Results
SMA (Simple Moving Average) and SES (Simple Exponential Smoothing) show good performance, but the Holt-Winters Exponential Smoothing method yields the best results with the lowest error metrics, making it the most accurate model for forecasting Google stock prices.

## Conclusion
The Holt-Winters Exponential Smoothing method is selected as the final model due to its superior performance in terms of MAE, MSE, RMSE, and MAPE. This model accounts for both trend and seasonality, providing a reliable forecast for Google stock prices.

