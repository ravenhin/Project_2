# Predicting Subreddits

In order to predict which posts were coming from certain subreddits, I created three different kinds of models and ran different parameters on each of these models. I choose subreddits from two political candidates that are running for the democratic nomination. I wanted to see if it was easy for a model to choose which posts came from a certain subreddit.

### Exploring the Data: Bernie and Biden, 2-word phrases

The top two word phrase from SandersforPresident subreddit:
  "Bernie Sanders"

The top two word phrase from JoeBiden subreddit:
  "Joe Biden"

Each one of these subreddits had the candidate mentioned in their top 25, 2 word phrases.
In looking at the two word phrases, I thought I would see more issues come through but it is mostly mentions other people related to the presidential race.

Below I have put the scores from each of the different kinds of models.

### Best Scores of each model

|Model Type| Model Train Score| Model Test Score|
|----------|------------------|-----------------|
|Logistic Regression| .91| .87|
|KNeighbors| .87| .85|
|MultinomialNB| .84| .82|
|Random Forest| .98| .88|

### Best Parameters of each model

|Model Type| Maximum Dataframe| Minimum Dataframe| Maximum Features|
|----------|------------------|------------------|-----------------|
|Logistic Regression| 98%| 3 words| 500 features|
|KNeighbors| 98%| 2 words| 100 features|
|MultinomialNB| 98%| 2 words| 400 features|
|Random Forest| 95%| 3 words| 500 features|

In conclusion, the best model for predicting which post came from a certain subreddit was the Random Forest. The random forest is best for this kind of classification model because of the size of features this data contains as well as the fact that this is a classification problem being solved. While all the models I ran are used for classification, Random Forest is the best because of how it uses sampled features of decision trees, which are weak learners, and takes in the case 100 resampled samples with replacement to make a strong prediction.
