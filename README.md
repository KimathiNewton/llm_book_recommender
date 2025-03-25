## How word3vec works

* Skipgram architecture

The way the word embeddings work is by taking all usages of each word in the training data, and trying to predict which words are likely to sorround it.

We start by transforming each of the words into words embeddings, but we then add positional vectors to this word embeddings, to indicate the position in the sentence. This weighted word embeddings are then fed into a mechanism called self attention. Self attention basically uses the information from the weighted word embedding to understand how much attention it needs to pay to the other words in the sentence in order to get the meaning of that word.
The model creates these self attention vectors for each word multiple times and then averages it. Then the model does some normalization which makes it easier to work with these attention vectors.
The process of generating self attention vector and then normalizing them is called an encoder vector. 