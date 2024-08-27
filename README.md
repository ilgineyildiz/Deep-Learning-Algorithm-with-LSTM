# Airline Passengers Prediction Using LSTM
This project involves building an LSTM (Long Short-Term Memory) model to predict the number of airline passengers over time using a time series dataset. The dataset is obtained from the famous airline passengers dataset, which records monthly totals of international airline passengers from 1949 to 1960.

## Project Overview
Time series forecasting is a crucial aspect of various domains, such as finance, weather forecasting, and inventory management. In this project, we demonstrate the use of LSTM, a type of recurrent neural network (RNN) particularly suited for sequential data, to predict future values in a time series.

### 1. Data Preprocessing
The dataset is loaded from a CSV file.
The data is normalized using MinMaxScaler to bring all values into the range [0, 1], which is essential for improving the performance of the LSTM model.
The dataset is split into training (80%) and testing (20%) sets.
The data is restructured into a supervised learning format, where the previous time_step values are used to predict the next value.

### 2. LSTM Model
Architecture:
Two LSTM layers with 50 units each.
A Dense layer with a single neuron for the output.
The model is compiled with the Adam optimizer and mean squared error (MSE) as the loss function.
The model is trained for 20 epochs with a batch size of 1.

### 3. Predictions
After training, predictions are made on both the training and testing datasets.
The predicted values are then inverse transformed to their original scale for comparison with actual values.

### 4. Evaluation Metrics
Mean Absolute Error (MAE): Measures the average magnitude of the errors in a set of predictions.
Mean Squared Error (MSE): Measures the average of the squares of the errors.
Root Mean Squared Error (RMSE): The square root of the average of squared errors.

The performance metrics for this model are:
Train MAE: 19.21
Test MAE: 44.85
Train MSE: 616.09
Test MSE: 3112.68
Train RMSE: 24.82
Test RMSE: 55.79

### 5. Visualization
A plot is generated to visualize the actual data alongside the predicted values for both the training and testing sets, providing a clear view of the model's performance.

### 6. Model Saving
The trained LSTM model is saved to a file named air_passenger_lstm_model.h5, which can be loaded for future predictions without retraining.

### Dependencies
Python 3.x
TensorFlow
scikit-learn
Matplotlib
NumPy
Pandas

### Running the Project

Clone the repository:
git clone https://github.com/yourusername/airline-passenger-prediction.git
cd airline-passenger-prediction

Install the required dependencies:
pip install -r requirements.txt

Run the Python script:
python lstm_airline_passengers.py

The script will train the model, generate predictions, display a plot of the results, and print evaluation metrics to the console.

### Conclusion
This project showcases the application of LSTM networks for time series forecasting. Despite the complexity of sequential data, the LSTM model effectively captures the underlying patterns in the airline passengers dataset, providing reasonably accurate predictions for both training and testing datasets.
