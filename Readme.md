# Stock Price Prediction with Recurrent Neural Network (RNN)

This project demonstrates the use of Recurrent Neural Networks (RNNs) to predict stock prices, specifically focusing on Google's stock prices in this example.

## Overview

Stock price prediction is a common application of RNNs in the field of time series forecasting. The goal is to use historical stock price data to predict future prices. In this project, we use a specific type of RNN known as Long Short-Term Memory (LSTM) to make these predictions. [Code File.](https://github.com/VrajMalvi/Google-Stock-price-prediction/blob/main/Google_Stock_price_prediction_RNN_LSTM.ipynb)

## Procedure

### Data Preprocessing

1. **Importing the Data**: We start by importing the training data from the 'Google_Stock_Price_Train.csv' file.

2. **Feature Scaling**: We use Min-Max scaling to normalize the stock price data to a range between 0 and 1.

3. **Creating Sequences**: We create sequences of stock prices with 60 time steps in the past and use them to predict the next price. This involves organizing the data into input sequences (X) and output labels (y).

### Building and Training the RNN

4.**Building the RNN**: We construct an LSTM-based RNN model with multiple layers. The `return_sequences` parameter is set to `True` for intermediate layers to capture the sequence of hidden states.

5.**Compiling and Training**: The model is compiled with an optimizer (e.g., Adam) and a loss function (mean squared error). We fit the model to the training data over multiple epochs.

### Making Predictions

6.**Getting Real Stock Prices**: We import the test data for January 2017 ('Google_Stock_Price_Test.csv') to obtain the real stock prices.

7.**Predicting Stock Prices**: To predict January data, we need the previous 60 days' data. We concatenate the training and test data and reshape it. We then use the trained model to predict stock prices for January.

### Visualizing the Results

8.**Visualizing Predictions**: We use Matplotlib to visualize the predicted and real stock prices for January 2017. The results are shown in a line chart.

## Model Evaluation

![Model Output Trend](https://github.com/VrajMalvi/Google-Stock-price-prediction/blob/main/picture/Screenshot%202023-12-01%20at%205.23.28%E2%80%AFPM.png)

In this model, our focus is on examining the trend of both the test and train data instead of relying solely on metrics like Root Mean Squared Error (RMSE). The graphical representation reveals that the predicted values align with the actual values, highlighting our emphasis on capturing the trend rather than evaluating based on RMSE scores.
