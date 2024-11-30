# Multivariate LSTM for Stock Price Forecasting of Big Tech Companies Using Time Series Data

This repository contains a Jupyter notebook that demonstrates how to use a Multivariate Long Short-Term Memory (LSTM) model to predict stock prices. The model is developed using Python and TensorFlow/Keras, and it utilizes historical stock data.



## Overview

Predicting stock prices is a challenging task due to the inherent volatility and complexity of financial markets. Traditional statistical methods often fall short in capturing the non-linear patterns present in time series data. Long Short-Term Memory (LSTM) is a type of Recurrent Neural Network (RNN) designed to overcome RNNs' limitations in capturing long-term dependencies in sequential data. LSTM introduces a memory cell and gates (input, output, and forget) to regulate information flow, enabling the model to retain important information over long sequences. This project aims to predict future stock prices by analyzing historical time series data using a Multivariate LSTM neural network.



### 1. Data Pre-processing

  * Load historical stock price data using the yfinance library.
  * Cleaning and formatting raw historical stock data.
  * Scaling data using MinMaxScaler to normalize features.
  * Splitting data into training and testing sets.

### 2. Model Development

  * Building a Sequential model with multiple LSTM layers.
  * Adding dropout layers to prevent overfitting.
  * Incorporating a dense layer for the final output.

### 3. Training and Evaluation:
   
   * Training the model on historical data.
   * Evaluating the model's performance using Mean Squared Error (MSE).
   * Visualizing predictions against actual stock prices ( from the test set) to assess the model's accuracy.

## Model Explanation

The Multivariate LSTM model used in this project is designed to capture complex temporal dependencies in the data. Unlike univariate models that predict based on a single feature, this model takes multiple features into account, allowing it to learn richer patterns in the stock market data.

  * **LSTM Layers:** These layers are adept at handling sequences of data and can retain information over long periods, making them ideal for time series forecasting.
  * **Dropout Layers:** To prevent overfitting, dropout layers are added between LSTM layers, which randomly ignore some of the input units during training.
  * **Dense Layer:** The final dense layer outputs the prediction for the next time step based on the learned features.

## Results

The model's predictions are visualized alongside the actual stock prices to give a clear indication of its performance. The Mean Squared Error (MSE) is calculated to provide a quantitative measure of accuracy.


## Hyperparameter Tuning

Explore different architectures by adding more LSTM layers or adjusting the number of units in each layer. Fine-tune the model by varying the number of epochs, batch size, and optimizers to enhance performance.

## Deployment

The model was deployed through a microservice API, allowing for real-time stock price prediction, and it has been updated in a separate [repository](https://github.com/saifx19/stock-price-prediction-api).
