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

Methology and Results:
  - After training, hyperparameters tuning and comparing two models, TFIDF with SVM is the winner model. C=10 and gamma=0.1 are the best parameters for RBF SVM kernel on which classifier is based.
  - The balanced accuracy, precision and recall for it are: 0.81, 0.91, 0.89.
  - In TFID, the text is vectorized based on the no of times a word occurs in a document, count of the word across a documents and total no of documents.
  - So, the vectorized text is the training input for the SVM classifer.
  - BERT based model performed decent better than baseline TFIDF SVM classifier.
  - For it text were tokenized and padded into a uniform sequences.
  - Then they were transformed into tensors and shuffled before putting them into training in batches of size = 32.
  - BERT model was optimized using ADAM with sparse categorical cross entropy as the loss function.
