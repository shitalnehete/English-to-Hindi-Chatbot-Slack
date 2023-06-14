# English to Hindi Language Translator
This repository contains a Seq2Seq model developed using Keras' LSTM with attention mechanism to convert English sentences into Hindi language. The model utilizes an encoder-decoder architecture for translation tasks.

## Dataset
The dataset used for training and testing the model was collected from http://www.manythings.org/anki/. The data was preprocessed to extract source and target pairs, where English sentences were paired with their corresponding Hindi translations. This paired data was used to train the Seq2Seq model.

## Data Preprocessing
Before feeding the data into the Seq2Seq model, it underwent several preprocessing steps. The data was tokenized, splitting sentences into individual words or subwords, to provide inputs to the encoder and decoder. One-hot encoding was then applied to convert the tokenized data into vectors, which served as the input for the models.

## Model Architecture
The Seq2Seq model employed an LSTM-based encoder-decoder architecture. The encoder received the tokenized English sentences and encoded them into a fixed-length context vector representation. The decoder then took this context vector as input and generated the corresponding Hindi translations word by word, using attention mechanism to focus on relevant parts of the source sentence.

## Web Service and Deployment
To make the translation model easily accessible to users, a web service was built using Flask, a Python web framework. The web service allows users to input English sentences and receive the translated Hindi sentences as output. The service was then deployed on the Slack app using the Slack API, enabling users to interact with the translation model directly on the Slack platform.

## Usage
To use the English to Hindi Language Translator, you can either access the web service through the deployed Slack app or integrate it into your own application. The translation model accepts English sentences as input and provides the corresponding Hindi translations as output.

Please refer to the code provided in this repository for detailed instructions on setting up the environment, training the model, and utilizing the translation service.
