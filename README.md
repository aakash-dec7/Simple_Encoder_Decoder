# Simple Encoder Decoder

## Overview
This project implements a simple Encoder-Decoder model using LSTM layers for sequence-to-sequence (seq2seq) learning. The model is designed for neural machine translation (NMT) tasks, translating English sentences into Spanish sentences. The Encoder encodes the input sentence into hidden states, and the Decoder uses these hidden states to generate the target sentence.

## Features
* Implements seq2seq architecture with LSTM layers for both Encoder and Decoder.
* Supports tokenization, padding, and batch processing.
* Ability to save and load training checkpoints.
* Configurable hyperparameters for flexibility in model design.
* Uses PyTorch for building and training the model.
* Implemented BLEU score evaluation to assess the performance of the model.

## Dataset
The dataset used for training consists of paired sentences in English and French.
Data Preprocessing includes:
* Adding special tokens (`<sos>` and `<eos>`) to target sentences.
* Tokenization and padding of sentences to a maximum length.
* Conversion of tokenized data into PyTorch tensors for training.

The dataset should be stored in a CSV file named eng_spn.csv, with two columns:
* English words/sentences
* Spanish words/sentences

## Architecture
The model consists of the following components:

**1. Encoder**
* Embedding Layer: Maps input tokens to dense vectors.
* LSTM Layer: Encodes input sequences into hidden and cell states.
* Dropout Layer: Prevents overfitting by randomly deactivating neurons during training.

**2. Decoder**
* Embedding Layer: Maps target tokens to dense vectors.
* LSTM Layer: Generates decoded sequences based on the Encoder's hidden states and the previous target tokens.
* Linear Layer: Maps LSTM outputs to target vocabulary logits.
* Dropout Layer: Prevents overfitting.

**3. Seq2Seq**
* Combines the Encoder and Decoder for end-to-end sequence prediction.

## Hyperparameters
Adjust these to customise your training:
* Sequence Length: `MAX_LENGTH = 25`
* Embedding Dimensions: `EMBEDDING_DIM = 128`
* Hidden Dimensions: `HIDDEN_DIM = 256`
* Layers: `NUM_LAYERS = 2`
* Dropout: `DROPOUT = 0.3`
* Batch Size: `BATCH_SIZE = 64`
* Epochs: `NUM_EPOCHS = 50`
* Learning Rate: `LEARNING_RATE = 0.001`

## Contributions
Feel free to fork the repository and submit a pull request for improvements.

## License
This project is licensed under the MIT License.
