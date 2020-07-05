# Ads Click Through Rate Prediction for Streaming Data In Apache Spark

what is the CTR?  
CTR = (click) / (impression)

## Project Summary
In this project, I just handle the cold start issue without users' historical data and demography. I mainly focus on using context feature to predict the probablity of a user who will click the Ads or not. Moreover, I also bring streaming mechanism to illustrate how to simulate streaming data to monitor model performance and CTR changes in real-time.

## 0. Data Pipeline  
![](My%20Folder/ML%20Pipeline.png)


## 1. Data Exploration
In this section, I use Spakr SQL to write some queries to get some initial view of the important features' distribution such as Banner position, device type, site_category, hour of a day and so on.


## 2. Feature Engineering
Before I move further to deploy machine learning models, I need to set bins to split continuous variables into categorical variables in order to improve model performance. After checking the data schema, I find out that all of the feature variables are string type, so I can use stringindexer and VectorAssembler API to map the string type variables into vector type.



