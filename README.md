# Reddit_Flair_Prediction

A web application to detect flair of a given Reddit r/india post.

## Contents

1. [Data Collection](https://github.com/raghav103/Reddit_Flair_Prediction/blob/master/Reddit-Flair-Predictor-DataCollection.ipynb) : This notebook contains the code to scrape data from reddit and make a dataset.
2. [Data Analysis](https://github.com/raghav103/Reddit_Flair_Prediction/blob/master/Reddit-Flair-Predictor-DataAnalyses.ipynb) : This notebbok contains the code to explore, clean, analyse dataset.
3. [Flair Prediction](https://github.com/raghav103/Reddit_Flair_Prediction/blob/master/Reddit-Flair-Predictor-Models.ipynb) : This notebook contains code to test various Machine Learning and Deep Learning models on our dataset.

## Approach 💡

After Extraction and cleaning of dataset I applied various Machine Learning and Deep Learning model to get good accuracy.

### Choosing the best features and applying Baseline models

To find the best combination of features, I used Bag of Words model. First text was converted to Tf-idf vectors and then these vectors were fed to the following models :-

1. #### Linear SVC
2. #### Naive-Bayes
3. #### Logistic Regression
4. #### Random Forests
