# Project Overview
  Text Comprehension, Question and Answering, Generative Text and Sentiment Analysis have all made great strides throughout the past decade - and progress is only accelerating. Does there exist, though, a model which can predict `sarcasm`? The difficulty in doing so is that we may not be able to do so with current methods as the type and amount of context that is necessary is not accounted for. There are two key indicators of sarcasm:
  
1) A shared knowledge between the speaker/writer and listener/reader
   i) eg. It's -30 degrees and windy -> "Beautiful day today, isn't it?"
3) The speaker/writer's intent
   
  We may or may not be able to access this shared knowledge, but maybe through NLP techniques we may infer the writer's intent. This project strives to utilize machine learning and neural networks to predict the occurence of sarcasm in a given text. In doing so it will allow users to know whether a given input is genuine or misleading. 

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Dataset
The data was gathered by Mikhail Khodak and Nikunj Saunshi and Kiran Vodrahalli by scraping `reddit` comments between the years of 2009 to 2017. The data contains ~1 million comments
evenly split by the labels `0` for non-sarcastic and `1` for sarcastic. The labels were generated using self-annotation, meaning the author of the comment added an `/s` tag at the end of their post to indicate that they were being sarcastic. Other than the comments and labels, the dataset also contains:

- author: the creator of the comment
- subreddit: which reddit forum it was posted on
- score: the net `upvote` - `downvote`
- ups: the amount of `upvotes` (likes)
- downs: the amount of `downvotes` (dislikes)
- date: the year and month comment was created
- created_utc: the date and time comment was created
- parent comment: the comment that preceeded it

**Data can be found** on Kaggle [here](https://www.kaggle.com/datasets/danofer/sarcasm) and Google Drive [here](https://drive.google.com/file/d/1Idd2QZ8fawKfeUFxmWTNeMsPSUS4XQgo/view?usp=drive_link).
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Project Workflow

## Data Cleaning
- searched for and removing negligible amount of duplicates and null values
- converted data to appropriate datatype
- eliminated redundancies

## EDA
- looked for patterns and relationships in data
- isolated sections related to our target variable
- found words associated with sarcasm

## Preprocessing
- removed unncessary features, including all non-text columns
#### Fitting and transforming text data using:
- Count Vectorizer
- TF IDF
- Word2Vec self-trained
- Word2Vec pre-trained


## Models --> Accuracy Score
- Logistic Regression with Count Vectorizer --> 0.65
- Logistic Regression with Count TFIDF --> 0.65 
- KNN using TFIDF --> 0.56
- MLP using self-trained Word2Vec --> 0.71
- MLP using Glove-Twitter-200 --> 0.68
- MLP using Word2Vec Google News --> 0.68

** See Requirements.txt for libraries

