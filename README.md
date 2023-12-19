# Contextual-Word-Forecasting-using-LSTM

### Project Summary:

In this project, I developed a Next Word Prediction model using Long Short-Term Memory (LSTM) neural networks. The dataset used for training the model consisted of text data extracted from a text file containing information about visits by Prime Ministers to the United States.

### Data Preprocessing:

##### Tokenization:
I began by tokenizing the entire text corpus, breaking it down into individual words. This step is crucial for converting the raw text into a format suitable for training a neural network.

##### Building Input Sequences:
To create input sequences for the LSTM model, I divided the text data into paragraphs, treating each paragraph as a sequence. The dataset was split using the newline character ('\n') to obtain individual sequences. The goal was to predict the next word in each sequence based on the context provided by the preceding words.

### Model Architecture:

The neural network architecture was designed using the Keras library with the following layers:

Embedding Layer: This layer is responsible for mapping the words to dense vectors of fixed size (100 in this case), converting the tokenized words into a continuous vector space.

LSTM Layer: The LSTM layer with 150 units was employed to capture long-term dependencies in the sequential data. LSTMs are well-suited for tasks involving sequential information, making them an ideal choice for predicting the next word in a sequence.

Dense Layer: The output layer consists of as many neurons as there are total unique words in the dataset, and it uses the softmax activation function to generate probabilities for each word in the vocabulary.

### Model Compilation and Training:

After defining the architecture, the model was compiled using categorical cross-entropy as the loss function and the Adam optimizer. The training process involved fitting the model to the input sequences and their corresponding target words.

The training was carried out for 100 epochs to ensure the model learned the patterns and dependencies present in the data. The training accuracy and loss metrics were monitored to assess the model's performance.

### Conclusion:

In conclusion, with the accuracy of 98%, the developed Next Word Prediction model using LSTM successfully learned the patterns in the dataset, enabling it to generate coherent predictions for the next word in a given sequence, particularly focusing on Prime Minister visits to the United States.
