# Ads Click Through Rate Prediction for Structured Streaming Data In Apache Spark


# Project Summary
In this project, I just handle the cold start issue without users' historical data and demography. I mainly focus on using context feature to predict the probablity of a user who will click the Ads or not. Moreover, I also bring streaming mechanism to illustrate how to simulate streaming data to monitor model performance and CTR changes in real-time.

## 0. Data Pipeline  
![](My%20Folder/ML%20Pipeline.png)


## 1. Data Exploration
In this section, I use Spakr SQL to write some queries to get some initial view of the important features' distribution such as Banner position, device type, site_category, hour of a day and so on.


## 2. Feature Engineering
2.1 Before I move further to deploy machine learning models, I need to set bins to split continuous variables into categorical variables in order to improve model performance. After checking the data schema, I find out that all of the feature variables are string type, so I can use stringindexer and VectorAssembler API to map the string type variables into vector type.  

2.2 For Deep Learning Model, I implement MinMaxScaler and OneHotEncoding API to process raw data, and them set all of the processed data as embedding feature for studying low and high dimension features interaction.  

## 3. Model Selection
### 3.1 Machine Learning Model -> Logistic Regression + Gradient Boosted Tree Classfier.  

Architecture:  

<img src="https://miro.medium.com/max/1400/1*jC5T3FeI_X8Zwa-rbf8cfg.png" width="500">

<img src="https://miro.medium.com/max/1400/1*ivIuVXL7JpnJx83DqWI9GQ.png" width="500">

<img src="https://miro.medium.com/max/1400/1*XzLBOdDH0ypuY0Ez8p9nKA.png" width="500">




### 3.2 Deep Learning Model -> DeepFM -> Factorization Machine + Deep Neural Network.  


Architecture:  

<img src="https://raw.githubusercontent.com/shenweichen/DeepCTR/master/docs/pics/DeepFM.png" width="600">


## 4. Structured Streaming and Evaluation.  

![](My%20Folder/streaming%201.png)

![](My%20Folder/streaming%202.png)

![](My%20Folder/streaming%203.png)

![](My%20Folder/streaming%205.png)
              

