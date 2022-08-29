# Sarcasm-Detection
The repository contains an implementation to detect sarcasm in news headlines and identifies whether the comments are sarcastic or not.  
I used two approaches for the classification task:  
#### 1) CNN-BiLSTM  
The model comprises of CNN layer followed by a bidirectional LSTM layer. The
CNN layer detects 128 properties and has ReLU as the activation function. The
LSTM layer has 64 nodes followed by a dense neural net containing 1 hidden
layer. The hidden layer has 100 nodes and contains L1 regularization. Dropout
layer of 0.1 has been used. The final output layer has a single node and activation
function Sigmoid has been used as we have to do binary classification.  
The model is trained for 10 epochs and achieves an accuracy of 93.33% with GloVe embeddings and 93.58% without them.
#### 2) BERT
This model uses a BERT pretrained encoder called ‘bert-case-uncased’. A neural
network consisting of 1 hidden layer has been implemented on top of the BERT
encoder. The hidden layer consists of 128 nodes with activation function of ReLu. A
dropout layer of 0.1 has also been implemented. The output layer has a single
node and activation function of sigmoid has been used as we have to do binary
classification.  
The model is trained for 10 epochs and achieves an accuracy of 95.23%.

### Dataset  
Both the [datasets](https://www.kaggle.com/datasets/rmisra/news-headlines-dataset-for-sarcasm-detection) are sourced from Kaggle.
