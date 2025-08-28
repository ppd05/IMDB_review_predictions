IMDB Review Sentiment Prediction
Overview

This project applies natural language processing (NLP) techniques to predict the sentiment of IMDB movie reviews. The objective is to classify reviews as positive or negative using Word2Vec embeddings combined with a deep neural network. The workflow includes preprocessing, word vectorization, model training, and evaluation.

Dataset
Source: IMDB Movie Review Dataset (50,000 labeled reviews)

Labels:
1 → Positive Review
0 → Negative Review

Preprocessing
The following text preprocessing steps were applied:

Text cleaning and normalization
Removal of HTML tags, URLs, emails, numbers, and special characters
Lowercasing
Handling contractions (e.g., don’t → do not)
Tokenization and stopwords removal
Tokenization using NLTK
Stopwords and very short tokens removed
Lemmatization
POS-based lemmatization using WordNet
Vocabulary filtering
Rare words with frequency < 2 removed

Feature Extraction
Word2Vec embeddings using Gensim
Vector size: 100

Review representation: average of Word2Vec vectors for tokens in each review

Model
A deep feedforward neural network was built using TensorFlow/Keras:


Metrics:

Accuracy, Precision, Recall, F1-score (classification report)
Confusion Matrix visualization
