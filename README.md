# Simple Encoder Decoder

This repository contains a sequence-to-sequence(Seq2Seq) model for Neural Machine Translation, implemented in PyTorch. The model uses an LSTM-based architecture to translate sentences from English to French(or any other language with a comaptible dataset).

## Features
* Encoder-Decoder architecture with LSTM layers.
* Tokenization and padding using Keras preprocessing.
* Training Checkpoints for resuming interrupted training.

## Dataset
The project uses a CSV file named `eng_spn.csv` containing two columns:
* **English words/sentences**: Input sentences in English.
* **French words/sentences**: Target sentences in French, with special tokens `<sos>` and `<eos>` marking the start and end of sequences.

## Architecture
* **Encoder**: Embedding layer -> LSTM -> Hidden states
* **Decoder**: Embedding layer -> LSTM -> Fully Connected Layer -> Output tokens
* **Seq2Seq**: Integrates Encoder and Decoder

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
