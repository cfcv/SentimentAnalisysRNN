# SentimentAnalisysRNN
## Requirements
The basic requirements to run this project is to have installed:
Python 3, jupyter notebook, Keras and Numpy.
 
## Description
The objective of this project is to build and train a RNN that given a
movie comment it can predict if it's positive or negative.

This project was divided in 5 main steps:
* 1: Loading the dataset
* 2: Preparing the data
* 3: Building the graph
* 4: Training
* 5: Testing

#### Loading the dataset
In this part we load two datasets files, first the file with the reviews(files.txt) and the labels
corresponding to each review(labels.txt)

#### Preparing the data
In the first moment we need to prepare the data to pass throught the network, first we get rid of
all the punctuation signs and create a list of reviews and labels. Next we have to create a dictionary to convert each word into a number and finally adjust the length of each review to 200 words, if the comment has fewer words it will be padded with zeros, otherwise it will be truncated. After the data is ready we can now separete our dataset in training, testing and validation sets(training: 80%, validation: 10%, test: 10%).
Training set -> 20000
Validation and Test set -> 2500

#### Building the graph
In this part i build the tensorflow graph with the following hyperparameters:
* lstm_size = 256  -> number of lstm cells
* lstm_layers = 1  -> number of layers
* batch_size = 500
* learning_rate = 0.001
* epochs = 10
* embed_size = 300 -> number of units in the embedding layer 

#### Training
Now that we've built our graph, we need to train the network, i trained in 10 epochs
and show the training loss in every 5 iterations and showing the accuracy in each 25 iterations.


#### Testing
Here i feeded the RNN with the test set to see how good is it. With this parameters
i've got a accuracy of 83,3%
