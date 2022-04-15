# yelpFakeReview

## Description

Trial different machine learning algorithms to improve fake review filter

## Getting Started

### Dependencies

* pandas, spacy, sklearn, gensim

### Database
 
* 600K Yelp reviews from Kaggle

### Details

* preProcessing:
```
cleaning(doc): lemmatize and remove stop words by spacy
w2v_model: create Word2Vec vocabularies
```
* trainingModel:
```
cleaningText(txt): cleaning(doc) + remove non-verbal
MeanEmbeddingVectorizer: average the fake and real Word2Vec vocabularies, transform the n reviews into vectors nxN: N is an average of 2 vectors from 2 different vocabularies fake and real
shuffleData(dfIn, colID): select/shuffle samples in dataframe 
```
### Word Vectorizer:

* Word2Vec

* TFIdf

### Testing models:

* MLPClassifier: overfitting
* MultinomialNB: ~60-68% accuracy
* LogisticRegression: ~60-68% accuracy
* ExtraTreesClassifier: 

## Acknowledgments

* Data creator: Shebuti Rayana and Leman Akoglu




