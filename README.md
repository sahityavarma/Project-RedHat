# Project-RedHat

# Predicting RedHat Business Value

**Problem Statement : Classify accurately to identify which customers have the most potential and Business value for RedHat based on their characteristics and activities**


![REDHAT](https://user-images.githubusercontent.com/51218875/155869079-3d1ad993-399a-4fab-8c8b-4d259ac1b46c.png)


Importance:
RedHat prominently delivers Customer Centric Solutions effectively in order to be the catalyst in communities of customers, contributors, and partners creating better technology in the open source way, It is very important to understand who are the most potential customers who add a value to their mission statement .Eventually by solving the problem we can understand the business value outcome which can be defined by a yes(1)or no(0) uniquely onto each activity in the data which helps Red hat build flexible, powerful IT infrastructure solutions. Red Hat plans to use these prediction models to efficiently prioritize resources by knowing their customers to generate future business and serve them by better understanding the Pre,Present and Post Journeys of different types of customers. Businesses can be better equipped to develop successful strategies by supporting the customers which is directly proportional in adding the real value to their way.

Technologies Used:
Python 2.7
RFE
Logistic Regression
Random Forest Classifier

Deployments :
Aws
Heroku

Key metric (KPI) to optimize in our scenario is ROC curve 

Data Acquisition:
The dataset was taken from https://www.kaggle.com/c/predicting-red-hat-business-value/data. It includes people.csv, act_train.csv and act_test.csv. 

Methodology/Approach:
This Scenario can be solved by using the Binary classification approach

Preprocessing:
1)Convert the categorical values into numerical ones
2)Convert boolean attributes to numerical ones
3)Break date column into three separate columns, namely date, month, and year
4)Imputing missing values for few columns with mode
5)Merge people and activity files
6)Separate the data and labels

Univariate ,Bi&MultiVariate analysis is done for data visualisation
Splitting Data into Training and Test Sets
**Model Building & Evaluation**
Comparision of Various Models After Modelling
AUC scores for Random Forest ,Decision tree & Adaboost are more when compared to other models. We can see that almost all the models performed more or less good.Random Forest model with hyperparameter tuning gave the best score out of all the models on both train and test data(Sensitivity).Eventually after observing all the model algorithm performance scores , we choose Decision tree model for deployment purpose rather than random forest because it requires low computation, thus reducing time to implement.

