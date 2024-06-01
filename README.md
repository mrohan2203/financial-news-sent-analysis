# Financial News Sentiment Analysis

## Objective
The goal of this project is to perform sentiment analysis on financial news articles and compare the performance of two different machine learning models: a Random Forest classifier and an LSTM (Long Short-Term Memory) neural network. The models will be evaluated based on their accuracy in predicting the sentiment of the news articles.

## Data Collection
Financial news articles were collected using the NewsAPI, focusing on articles containing the keyword "finance". The collected data includes publication date, title, description, and content of the articles.

## Data Preprocessing
1. Text Preprocessing:

Combined the title, description, and content into a single text column.
Removed HTML tags, punctuation, and numbers.
Converted text to lowercase.
Tokenized the text and removed stopwords.
Lemmatized the words to reduce them to their base form.

2. Handling Missing Values:

Filled missing values in the text column with empty strings.
Feature Extraction
For the Random Forest model, TF-IDF (Term Frequency-Inverse Document Frequency) vectorization was used to convert the preprocessed text into numerical features.

## Model Implementation
1. Random Forest Model:

TF-IDF vectorized text data was split into training and test sets.
A Random Forest classifier was trained on the training data.
Model evaluation was performed using accuracy score, classification report, and confusion matrix.

2. LSTM Model:

Tokenized the text data and padded the sequences to a consistent length of 100.
Split the padded sequences into training and test sets.
Built an LSTM neural network with an embedding layer, spatial dropout, LSTM layer, and a dense output layer.
Compiled and trained the model using binary cross-entropy loss and Adam optimizer.
Evaluated the model using accuracy score, classification report, and confusion matrix.

## Results
Both models were evaluated on the test data to compare their performance in terms of accuracy and other classification metrics. 

## Conclusion
This project successfully implemented and compared the performance of a Random Forest classifier and an LSTM neural network for sentiment analysis of financial news. The evaluation metrics provided insights into the strengths and weaknesses of each model, guiding further improvements and potential applications in financial sentiment analysis.

## Future Work
Future enhancements could include:

Using more sophisticated text embeddings like Word2Vec or BERT.
Tuning hyperparameters of both models for improved performance.
Exploring additional features such as article metadata or using different datasets for more robust sentiment analysis.
By leveraging machine learning techniques, this project demonstrates the potential to automate the analysis of financial news sentiment, which can be valuable for investors, analysts, and financial institutions.
