# news-classifier

In this project, we create and study news classifiers that classifies a news text into one of 4 categories: politics, arts, business, sports. The classifiers are trained on news from DW News (www.dw.com).

There are 3 primary goals for this project:
  - Data acquisition using selenium from dw.news to acquire training data
  - Create classifiers and select winning model
  - Topic modeling of news data acquired on each category

Two algorithms are train which are as follow:
  - Fine tuned BERT classifier based on a pre-trained uncased bert model
  - TFIDF with SVM

Preprocessing of the data before training includes:
  - Stop words removal
  - Tokenization, lemmatization
  - Grouping similar categories of news 
