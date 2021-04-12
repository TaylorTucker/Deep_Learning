# LSTM Stock Predictor

![deep-learning](https://thumbor.forbes.com/thumbor/960x0/https%3A%2F%2Fblogs-images.forbes.com%2Fkevinmurnane%2Ffiles%2F2016%2F03%2Fgoogle-deepmind-artificial-intelligence-2-970x0-970x646.jpg)


Due to the volatility of cryptocurrency speculation, investors will often try to incorporate sentiment from social media and news articles to help guide their trading strategies. One such indicator is the [Crypto Fear and Greed Index (FNG)](https://alternative.me/crypto/fear-and-greed-index/) which attempts to use a variety of data sources to produce a daily FNG value for cryptocurrency. I have attempted to build and evaluate deep learning models using both the FNG values and simple closing prices to determine if the FNG indicator provides a better signal for cryptocurrencies than the normal closing price data.

With 2 models, I used deep learning recurrent neural networks to model bitcoin closing prices. One model will use the FNG indicators to predict the closing price while the second model will use a window of closing prices to predict the nth closing price.

### Models

1. Fear and Greed model
2. Closing Price model


### Steps

1. [Prepared the data for training and testing](#prepare-the-data-for-training-and-testing)
2. [Built and trained custom LSTM RNNs](#build-and-train-custom-lstm-rnns)
3. [Evaluated the performance of each model](#evaluate-the-performance-of-each-model)

- - -

## Process

For the Fear and Greed model, I used the FNG values to try and predict the closing price. .

For the closing price model, I used previous closing prices to try and predict the next closing price. 

Each model used 70% of the data for training and 30% of the data for testing.

Applid a MinMaxScaler to the X and y values to scale the data for the model.

Finally, I reshaped the X_train and X_test values to fit the model's requirement of samples, time steps, and features. 

### Built and trained custom LSTM RNNs

I created the same custom LSTM RNN architecture. In one notebook, I fit the data using the FNG values. In the second notebook, I fit the data using only closing prices.

Use the same parameters and training steps for each model. This is necessary to compare each model accurately.

### Evaluatuation

Which model had a lower loss?
Answer:The model with the lower loss is the closing prices predictor
----------------------------
Which model tracked the actual values better over time?
Answer:The model with better results over time is the closing prices predictor
----------------------------
Which window size worked best for the model?
Answer:The window size that works better is 1

- - -

### Resources

[Keras Sequential Model Guide](https://keras.io/getting-started/sequential-model-guide/)

[Illustrated Guide to LSTMs](https://towardsdatascience.com/illustrated-guide-to-lstms-and-gru-s-a-step-by-step-explanation-44e9eb85bf21)

[Stanford's RNN Cheatsheet](https://stanford.edu/~shervine/teaching/cs-230/cheatsheet-recurrent-neural-networks)

- - -


