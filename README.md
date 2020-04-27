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

## Result 

### Tittle 
| Model  | Test Accuracy  |
|---|---|
| LinearSVC  | 0.6586826347305389  |
| Naive - Bayes  | 0.6167664670658682  |
| Logistic Regression  | 0.6616766467065869  |
| Random Forest Classifier  | 0.6377245508982036  |


### URL 
| Model  | Test Accuracy  |
|---|---|
| LinearSVC  | 0.4940119760479042  |
| Naive - Bayes  | 0.4281437125748503  |
| Logistic Regression  | 0.49700598802395207  |
| Random Forest Classifier  | 0.47305389221556887  |


### Comments 
| Model  | Test Accuracy  |
|---|---|
| LinearSVC  | 0.47474747474747475  |
| Naive - Bayes  | 0.3872053872053872  |
| Logistic Regression  | 0.47474747474747475  |
| Random Forest Classifier  | 0.3872053872053872  |


### Title + Comments + URL 
| Model  | Test Accuracy  |
|---|---|
| LinearSVC  | 0.7395209580838323  |
| Naive - Bayes  | 0.5538922155688623  |
| Logistic Regression  | 0.718562874251497  |
| Random Forest Classifier  | 0.6047904191616766  |


### Title + Body + URL
| Model  | Test Accuracy  |
|---|---|
| LinearSVC  | 0.7455089820359282  |
| Naive - Bayes  | 0.5538922155688623  |
| Logistic Regression  | 0.718562874251497  |
| Random Forest Classifier  | 0.5748502994011976  |

## Deep Learning 

- Deep Learning models can learn more complex functions than traditional Machine Learning models.
- I used the folowing models :-

### 1. Word Embeddings + CNN
      - CNNs are well known for there location invariant feature extraction capability, So I decided to use CNN model for text      classification. In hope that CNN model will learn some useful filters, which can be used to distinguish between different text categories

### 2. LSTMs
      -LSTMS perform really well on many NLP tasks, because of their ability to remember past information and learn context. While the CNN model tries to classify by learning distinguishing tokens or sequence of tokens. LSTMs on the other hand try to understand the text, they can learn relationships between tokens.
      -But LSTMs didn't perform as accepted, I think the reason for low accuracy is less data

### 3. Bidirectional LSTMs
      -Bidirectional LSTMs, are more effective than unidirectional ones. This is because training two LSTMs on the same input in forward and reverse direction allows the network to learn better context.
      -Bidirectional LSTM performed better than a unidirectional LSTM.

### 4. Hybrid-model CNN-LSTM
      -The idea was to combine the advantages of both models. The CNN would act as an effective feature extractor which would pass only the essential information to LSTM. And then LSTM model would learn interesting dependencies in data.

| Model  | Test Accuracy  |
|---|---|
| LinearSVC  | 0.7874251497005988  |
| Naive - Bayes  | 0.6047904191616766  |
| Logistic Regression  | 0.625748502994012  |
| Random Forest Classifier  | 0.6736526946107785  |

- LSTM based models lagged behind CNN and even traditional ML models like Logistic Regression and LinearSVC. I think the reason is less data LSTMs require large data to perform well.





