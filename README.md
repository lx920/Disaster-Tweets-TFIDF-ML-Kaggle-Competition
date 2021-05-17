# Disaster-Tweets--Kaggle-Competition
This is a Kaggle Competition aiming to correctly identify which tweets are related to real natural disasters.\
The competition is on-going, and the link is: https://www.kaggle.com/c/nlp-getting-started

# Dataset Brief
https://www.kaggle.com/c/nlp-getting-started/data \
The dataset contains 7613 tweets that may or may not be related to naturla disaster.\
The independent variable are unstructed texts within a tweet. \
The dependent variable we are predicting is 1 and 0. Disaster, and non-Disaster.
# Main Packages
- pandas, numpy, seaborn, matplotlib
- NLTK
- sklearn

# Steps of Project
1: Data Visualization\
2: Data Preprocessing\
3: NLP preprocessing\
4: Model Building

# Data Visualization
In this section, I used matplotlib to perform EDA on the dataset
- Classification class balance
- Distribution of tweet length
- Most Frequent Key words and stop words

# Data Preprocessing
Remove the garbage in the data!
- Use regexp to remove URLs, https, emoticons and signs.
- Remove stopwords in NLTK stopwords dictionary
- Perform porter stemming on texts
- set all texts to lowercase

# NLP Preprocessing
I decided to use TF-IDF over Bag of Words.
- Use TF-IDF vertorizor to turn cleaned tweets into vectors.
- set up n-gram as 1, and idf smoothing to deal with edge cases.

# Model Training
I applied 5 ML models on the TF-IDF processed data. And measured their performance.
- Logistic Regression \ 
0.80 accuracy score.
- Random Forest (Untuned) \
0.78 accuracy score \
could be better because I did not tune parameters, takes too long.
- XGBoost\
0.77 accuracy score
- Voting Ensemble\
Voting Ensemble consists of logistic regression, Naive Bayes and XGBoost \
0.82 accuracy score
- Naive Bayes \
0.81 accuracy score

# Conclusion and Submission
- The Voting Ensemble of LR + NB + XGB seems to have highest Accuracy Score
- Predicted Kaggle Test dataset and made submission
- Final submission score 0.794
