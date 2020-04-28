# Predicting the likelihood of popularity for news article

In this project, I will be crawling news websites to find articles and anticipate the likelihood of their virality. There hasn't been a significant amount of success in this field, with the best model not even hitting 70% accuracy. This project, done for the BiPolar Factory Internship, doesn't challenge that accuracy. However, there is another approach presented towards the end which I will consider in future projects that has the potential to beat this current accuracy.

I have used the famous( and actually, the only one dealing with news popularity) UCI dataset containing a heterogeneous set of features about articles published by Mashable in a period of two years. Link to dataset: http://archive.ics.uci.edu/ml/datasets/Online+News+Popularity 

The goal is to predict the probability of shares being greater than a certain popularity threshold(defined by taking median of shares column of dataset). Naturally, logistic regression( which I trained as a neural network using keras) is the way to go.

Since the model has to be used to predict this probability for web crawled raw data, feature selection becomes more than just a matter of which have the highest importance: I should also be able to extract them from web crawled data. As a result, my model's accuracy is lower than the current state-of-the-art model. However, given the sparsity and minimal importance of features I used, the model does a pretty good job with a K-fold cross validation accuracy of nearly 62.5%.

Towards the end, I have proposed another possible approach to news popularity. I shall investigate that in future projects.
