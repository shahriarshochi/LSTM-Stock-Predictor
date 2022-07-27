# LSTM-Stock-Predictor

Due to the volatility of cryptocurrency speculation, investors will often try to incorporate sentiment from social media and news articles to help guide their trading strategies. One such indicator is the Crypto Fear and Greed Index (FNG) which attempts to use a variety of data sources to produce a daily FNG value for cryptocurrency. Here, I will build and evaluate deep learning models using both the FNG values and simple closing prices to determine if the FNG indicator provides a better signal for cryptocurrencies than the normal closing price data.

## Methods and Techniques Used: 

### Prepare the data for training and testing

For the Fear and Greed model, I will use the FNG values to try and predict the closing price.

For the closing price model, I will use previous closing prices to try and predict the next closing price.

Each model will use 70% of the data for training and 30% of the data for testing.

I will be applying a MinMaxScaler to the X and y values to scale the data for the model.

Finally, I will reshape the X_train and X_test values to fit the model's requirement of samples, time steps, and features. (example: X_train = X_train.reshape((X_train.shape[0], X_train.shape[1], 1)))

### Build and train custom LSTM RNNs

In each Jupyter Notebook, I will be creating the same custom LSTM RNN architecture. In one notebook, I will fit the data using the FNG values. In the second notebook, I will fit the data using only closing prices.

I am going to use the same parameters and training steps for each model. This is necessary to compare each model accurately.

### Evaluate the performance of each model

Finally, the testing data will be used to evaluate each model and compare the performance.


## Goal Of This Project:

The main purpose of this project is to use deep learning recurrent neural networks to model bitcoin closing prices. The goal is to use a window of closing prices to predict the nth closing price.
