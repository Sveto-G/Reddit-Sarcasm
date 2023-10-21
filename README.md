# Project Overview
This project strives to utilize machine learning to predict the occurence of sarcasm in a given text. In doing so it will allow users to know whether a given input is genuine or misleading. 

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

**Data can be found** [here](https://www.kaggle.com/datasets/danofer/sarcasm)
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Project Workflow

## Data Cleaning
- searching for duplicates, null values
- converting data to appropriate datatype
- eliminating redundancies

## EDA
- looking for patterns and relationships in data
- isolating sections related to our target variable

## Feature Engineering
- transforming and refactoring data based off of given relationships in effort to fit model

## Modeling
**TO DO**
- TF IDF
- KNN
- Text Embedding

