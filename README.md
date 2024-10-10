# Apple Stock Price Prediction using Stacked LSTM

This project implements a **Stacked LSTM (Long Short-Term Memory)** model to predict the future prices of **Apple Inc. (AAPL)** stocks. The model is trained using historical stock data, which is retrieved from the **Tiingo API**.

## Project Overview

### Objective:
The primary goal of this project is to develop a machine learning model that can predict the future prices of Apple stocks based on historical data. The model employs **Stacked LSTM**, a recurrent neural network (RNN) architecture known for its ability to capture long-term dependencies in time series data.

### Data Source:
- **Tiingo API**: The stock data is fetched programmatically via the **Tiingo API**. Tiingo provides reliable and comprehensive financial data, which is used to train the model on historical prices of Apple stocks.
  
  **Note**: To use this API, you'll need to obtain an API key from Tiingo and set it up in the code.

### Model Architecture:
- **Stacked LSTM**: This model leverages multiple layers of LSTMs stacked on top of each other to improve its ability to learn complex patterns from time series data. LSTMs are particularly well-suited for financial time series forecasting due to their ability to remember important information over time.
  
- **Input Data**: The model is trained on the **closing prices** of AAPL stocks.
  
- **Output**: The model predicts the **future closing prices** of AAPL.

## Project Structure:

- **Data Preprocessing**: 
  - Historical stock prices are fetched using the Tiingo API.
  - The data is normalized and transformed into sequences to fit the input shape required by the LSTM model.
  
- **Model Training**: 
  - The Stacked LSTM model is built and compiled using **TensorFlow** and **Keras**.
  - The model is trained using the preprocessed stock data, with appropriate train-test splits.

- **Evaluation**: 
  - After training, the model’s performance is evaluated by comparing the predicted stock prices to the actual stock prices using metrics like **Mean Squared Error (MSE)**.

## Requirements:

### Libraries:
- **Python 3.x**
- **TensorFlow**: To build and train the LSTM model.
- **Keras**: As a high-level neural network API.
- **Tiingo API**: For fetching stock data.
- **Pandas**: For data manipulation and preprocessing.
- **NumPy**: For numerical computations.
- **Matplotlib**: For visualizing the stock prices and predictions.
  
### API Setup:
1. Create an account on [Tiingo](https://www.tiingo.com/) and obtain your API key.
2. Set up the API key in the code where necessary.

## How to Run the Project:

1. **Install the required libraries**:
   ```bash
   pip install tensorflow keras pandas numpy matplotlib requests
