# TimeSeries_StackingModels

This notebook is to predict the mean_temperature for the daily climate time series data. The data is available at:

https://www.kaggle.com/datasets/sumanthvrao/daily-climate-time-series-data

Here are methods I used in the notebook:

- SARIMAX: Seasonal ARIMA + exogenous variables.
- Prophet:
    - Univariate Prophet 
    - Univariate Prophet + XG Boost on the residuals
    - Univariate Prophet on differencing time series
    - Multivariate Prophet
- Vector error correction model (VECM)
- Long-short term memory (LSTM)
- Neural Prophet: Neural network version of Prophet.

# Results.

The best model for the problem is Prophet, both multivariate (with unknown wind_speed and humidity) and univariate version perform well. When combining with XG boost on the residuals, the results of Prophet is improved. There is a reason for it:

- Prophet excels at capturing trend and seasonality, including handling holiday effects and changes in trend.

- XGBoost excels at modeling complex, nonlinear relationships and interactions between features. By focusing on the residuals, XGBoost effectively hones in on the patterns that Prophet may overlook.

LSTM and neural Prophet also perform well, but those models, especially LSTM may need more data to shine.