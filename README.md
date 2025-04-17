We used daily closing prices for Litecoin (LTC) from the CoinGecko API, covering the past 365 days.
Preprocessing of the dataset in preparation for LSTM modelling was carried out as shown:

• Handling Missing Values: Check for missing values and fill them using forward filling.
• Smoothing: The IQR method was used for outlier detection and removal.
• Stationarity Check: Augmented Dickey-Fuller test has been performed, and diVerencing-whenever
required was performed to make the series stationary.
• Scaling: For this purpose, MinMaxScaler scaled the data between 0 and 1, suitable for LSTM.

The LSTM model captured the pattern of Litecoin's price very well. It showed a fairly moderate RMSE,
which normally reflects good prediction performance. Unlike ARIMA, LSTM adapts well to high
volatility and sequential dependencies of fluctuating markets.

In summary, LSTM works well in predicting both the trend and short-term movements. Possible further
enhancements could be the inclusion of GRU models or adding in trading volume and sentiment data
to improve the forecasts.
