# Demand-Forecasting-Using-Time-series
Project Report: Air Passenger Traffic Forecasting
Introduction:-
This project focuses on predicting the number of air passengers using historical time-series data. The task is framed as a classical time-series forecasting problem, where identifying underlying patterns such as trend, seasonality, and noise is critical for building accurate predictive models.

Data Preprocessing and Stationarity
Before applying forecasting models, the time-series must be stationary. A stationary series maintains:
A constant mean over time.
A stable variance or standard deviation.
Auto-covariance independent of time shifts.
To ensure stationarity, Augmented Dickey–Fuller (ADF) and KPSS tests were used. The ADF test checks for unit roots, with the null hypothesis being non-stationarity. A low p-value indicates that the null can be rejected, confirming stationarity. To further stabilize variance and reduce non-stationarity, a Box–Cox transformation was applied.

Trend and Seasonality Analysis
Non-stationarity in time series often arises due to trend (long-term upward or downward movements) and seasonality (recurring cycles). To capture these effects, the series was decomposed into:
Trend Component – long-term direction of growth or decline.
Seasonal Component – recurring fluctuations over regular intervals.
Residual Component – irregular or random variations.

Two decomposition models were explored:
1.Additive Model – suitable when both trend and seasonal effects change linearly over time.
2.Multiplicative Model – applied when trend and seasonality evolve at non-linear rates.

Forecasting Models
To model and forecast passenger numbers, several statistical models were used:
Holt-Winters Exponential Smoothing – incorporates level, trend, and seasonality in a weighted manner.
ARIMA (AutoRegressive Integrated Moving Average) – combines autoregressive (AR), differencing (I), and moving average (MA) components.
P (lags in AR) – captures dependence on past values.
D (order of differencing) – ensures stationarity.
Q (lags in MA) – accounts for past forecast errors.
SARIMA (Seasonal ARIMA) – extends ARIMA by incorporating seasonal lags for improved accuracy in cyclic data.
The AR component explains correlation across time periods, the MA component helps smooth noise, and differencing binds the model for long-term predictability.

Conclusion
Through rigorous statistical testing and model building, the project provides a structured approach to forecasting air passenger demand. By addressing stationarity, decomposing the series into meaningful components, and applying advanced models such as ARIMA and SARIMA, the study demonstrates how accurate time-series forecasting can be achieved for real-world applications.
