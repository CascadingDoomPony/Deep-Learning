# Deep-Learning

In this program we created an LSTM RNN model to predict the value of Bitcoin using historical price data and using a Fear and Greed (FNG) index using tensorflow. The models are tested and evaluated on each metric separately, but to compare perfomance the same model is used for both. We ensure they perform the same by setting random seeds for our tensorflow and numpy packages.

You can check the charts and code in the two jupyter notebook files.


## The Model

---

The model we used is three layers deep each with 30 units each, all with a dropout layer of 0.2 (20%).We compiled with an adam optimizer and using mean squared error as our loss function, then trained with 100 epochs with a batch size of 5. This setup gives relatively good performance without causing too much  overfitting or slowing down the training. 

## Testing

---

From our experimentation predicting from historical prices is relatively easy for most models we tried, as even though the prices do not match directly, the model usually captures the trend of the prices quite well. This particular model is quite accurate, and the priced are almost matching, just offset slightly

Predicting based off the FNG index on the other hand is quite difficult. We have tried changing the dropout fraction, nodes in each layer, and how many epochs we train on, and we struggle to create a model that captures the trend of the prices. Most of the models we create have a similar performance to the one on the file which we described above.