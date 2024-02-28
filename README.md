# ARIMA_Prophet_LSTM_TimeSeries

In this notebook, we will use ARIMA, Prophet, and LSTM to predict daily minimum temperatures. The data is available at:

https://www.kaggle.com/datasets/shenba/time-series-datasets?select=daily-minimum-temperatures-in-me.csv


Here are the main steps for the three models:

- ARIMA Model: First, we need to check check if the time series is stationary by plotting and using the ADF test. If it's non-stationary, we can apply differencing. The 'd' in ARIMA represents the number of differencing needed. Afterward, we can use ACF and PACF plots to determine the 'p' and 'q' terms in ARIMA. An easier approach is to employ auto ARIMA.

- Prophet: This model requires only two parameters: 'ds' (representing time) and 'y' (the minimum temperatures). There's no need to check for stationarity, as Prophet can adeptly handle seasonal and trend effects.

- LSTM: This neural network uses a gated architecture to manage information over long sequences, making it well-suited for time series prediction.

# Results

The best model for this problem is LSTM. However, Prophet is also a great choice when resources are limited (eg. GPUs).