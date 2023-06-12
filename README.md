# Google-Stock-Price-prediction-by-using-LSTM
The goal of this project is to demonstrate the use of RNNs, specifically LSTM (Long Short-Term Memory) layers, in forecasting stock prices based on historical data.

Data:
The model is trained on the Google stock price dataset, which includes 5 years (2012-2016) of train dataset and 1 month test dataset (Jan 2017) historical stock price data for Google. The dataset is preprocessed by scaling the stock prices using the MinMaxScaler from scikit-learn. The training set is divided into input sequences of 60 previous stock prices and their corresponding output stock price.

Model Architecture:
The RNN model architecture is designed to capture long-term dependencies in the sequential stock price data. It consists of four LSTM layers, each with 50 units, which allow the model to learn and remember patterns over extended sequences. Dropout regularization is applied after each LSTM layer to prevent overfitting and improve generalization. Finally, a fully connected output layer with a single neuron is added to predict the next stock price.

Training and Evaluation:
The model is trained for 100 epochs with a batch size of 32. The Adam optimizer is used to optimize the model parameters, and the mean squared error (MSE) loss function is employed as the training objective. During training, the model learns to minimize the difference between its predicted stock prices and the actual stock prices from the training set.

Visualization:
Once the model is trained, it is evaluated on the Google stock price dataset, which contains stock prices for a specific period. The predicted stock prices are inverse transformed to their original scale using the MinMaxScaler. To visualize the performance of the model, the actual and predicted stock prices for the test period are plotted using matplotlib. This allows for a visual comparison between the predicted and real prices, providing insights into the accuracy of the model's predictions.

This project serves as a practical example of utilizing RNNs and LSTM layers for stock price prediction. It demonstrates how historical stock price data can be leveraged to forecast future prices. You are encouraged to explore the code and adapt it to your own datasets and prediction tasks.
