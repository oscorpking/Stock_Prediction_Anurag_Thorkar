# Stock_Prediction_Anurag_Thorkar
The Stock Price Prediction project with LSTM Neural Network focuses on developing a reliable and accurate model for forecasting stock prices based on historical data. 


The provided code appears to be an implementation of a Long Short-Term Memory (LSTM) neural network for stock price prediction using historical data. Here's a breakdown of the code:

Importing the necessary libraries: The code begins by importing the required libraries, including pandas, numpy, matplotlib, and the necessary modules from the Keras library.

Reading and preprocessing the data: The code reads the stock price data from a CSV file using pandas and converts the "Date" column to datetime format. The "Close" column is then selected and scaled using the MinMaxScaler to ensure all values fall within the range of 0 and 1.

Splitting the data into training and validation sets: The dataset is split into training and validation sets. The first 987 data points are used for training, and the remaining data points are used for validation.

Creating input sequences: The code creates input sequences of length 60 for the LSTM model. Each input sequence contains the previous 60 days' closing prices as features, and the corresponding target is the closing price of the next day.

Building the LSTM model: The LSTM model is constructed using the Sequential API from Keras. It consists of two LSTM layers with 50 units each and a Dense layer with a single unit. The model is compiled with the mean squared error loss function and the Adam optimizer.

Training the LSTM model: The LSTM model is trained using the training data. The x_train_data (input sequences) and y_train_data (corresponding targets) are passed to the model for training.

Generating predictions: The code prepares the input data for generating predictions on the validation set. It reshapes the input data and scales it using the MinMaxScaler. Then, it predicts the closing prices using the trained LSTM model and inversely scales the predicted prices to their original range.

Saving the LSTM model: The trained LSTM model is saved as "saved_lstm_model.h5" for future use.

Visualizing the results: The code plots the training data's closing prices, along with the actual closing prices and predicted closing prices for the validation set.

It's important to note that the code only includes one epoch of training for demonstration purposes. In practice, you would typically train the model for multiple epochs to improve its performance.

Please ensure that you have the necessary dependencies installed and the CSV file ("NSE-TATA.csv") is available in the specified path before executing the code.
