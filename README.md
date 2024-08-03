# Energy consumption prediction of Finaland transmission system
## Time Series Forecasting (LSTM)

### Abstract

The purpose of this research was to predict energy consumption using data from Finland's transmission system operator. The objective was to assess whether a machine learning model could produce accurate results for a complex forecasting problem, by exploring various machine learning techniques and developing a data-driven model for energy forecasting.

The dataset consisted of six years of hourly electricity consumption in Finland, forming a univariate time series with seasonal patterns. A long short-term memory (LSTM) model was employed to train the data. The model's performance was evaluated using the root mean squared error (RMSE) to ensure comparability with the energy readings in the dataset.

The results demonstrate that electricity consumption can be effectively predicted using machine learning algorithms. These findings can facilitate the deployment of renewable energy, allow for better planning of high and low load days, and help reduce wastage from polluting standby reserve generation.

### Model Implementation
The data was imported from Finland's transmission system operator as a CSV file and then uploaded to a GitHub repository. The dataset contained a total of 52,965 observations and 5 variables, with no missing values. The load volume ranged from a minimum of 5,341 MWh to a maximum of 15,105 MWh, with an average volume of 9,488.750519 MWh. This dataset represented a univariate time series, requiring one column for time and another for energy consumption.

To predict daily consumption, the data was down-sampled from hourly to daily frequency using the resample function. The LSTM model was trained using this transformed dataset, with a training set and a validation set to test the results throughout the training process. The learning algorithm iterated through the entire training dataset 60 times (epochs), updating the model weights after each batch, with a batch size of 20.