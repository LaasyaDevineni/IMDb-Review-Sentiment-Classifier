# IMDb Review Sentiment Classifier

This repository contains a sentiment analysis model built using TensorFlow and Keras to classify movie reviews from the IMDb dataset into positive or negative sentiments.

## Table of Contents
- [Overview]
- [Model Architecture]
- [Training]
- [Results]
- [Usage]

## Overview
The IMDb Review Sentiment Classifier is designed to analyze movie reviews and predict the sentiment expressed in each review (positive or negative). The model uses recurrent neural networks (RNNs) with LSTM layers to process the text data effectively.

## Getting Started
To run this project, you need to have Python and the necessary libraries installed. You can install the required packages using the following command:

```bash
pip install tensorflow tensorflow-datasets matplotlib
```

## Model Architecture
The model architecture consists of the following components:

- TextVectorization Layer: This layer converts raw text into integer sequences, which makes it easier to process text data in neural networks.
- Embedding Layer: It transforms the integer sequences into dense vectors of fixed size, capturing semantic relationships between words.
- Bidirectional LSTM Layers: Two LSTM layers are used to process the sequences in both forward and backward directions, allowing the model to learn context from both ends of the text.
- Dense Layers: The final layers include dense layers that output the sentiment classification, with the last layer producing a single output for binary classification.

## Training
The model is trained on the IMDb dataset for a specified number of epochs (in this case, 5 epochs). During training, the model learns to minimize the loss function by adjusting its weights based on the predictions made on the training dataset. The training process involves the following key steps:
- Data Preparation: The dataset is divided into training and validation sets, allowing the model to learn from one portion while being evaluated on another.
- Compilation: The model is compiled with an appropriate optimizer and loss function suited for binary classification.
- Fitting the Model: The model is trained using the training dataset, with performance metrics tracked on the validation dataset. The training process involves adjusting the weights based on the computed loss and updating the model parameters accordingly.

## Results
After training, the model achieved an accuracy of 83.97% on the test dataset. This result indicates that the model correctly classifies approximately 84% of the movie reviews, demonstrating its effectiveness in sentiment classification.
