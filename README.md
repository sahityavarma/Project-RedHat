# Project-RedHat

# Predicting RedHat Business Value

**Problem Statement : Classify accurately to identify which customers have the most potential and Business value for RedHat based on their characteristics and activities**


![REDHAT](https://user-images.githubusercontent.com/51218875/155869079-3d1ad993-399a-4fab-8c8b-4d259ac1b46c.png)


Importance:
RedHat prominently delivers Customer Centric Solutions effectively in order to be the catalyst in communities of customers, contributors, and partners creating better technology in the open source way, It is very important to understand who are the most potential customers who add a value to their mission statement .Eventually by solving the problem we can understand the business value outcome which can be defined by a yes(1)or no(0) uniquely onto each activity in the data which helps Red hat build flexible, powerful IT infrastructure solutions. Red Hat plans to use these prediction models to efficiently prioritize resources by knowing their customers to generate future business and serve them by better understanding the Pre,Present and Post Journeys of different types of customers. Businesses can be better equipped to develop successful strategies by supporting the customers which is directly proportional in adding the real value to their way.

Technologies Used:
Python 2.7,
RFE,
Logistic Regression,
Random Forest Classifier,
Aws,
Heroku,
Anaconda Prompt.

Deployments :

Local Deployment


Aws(Cloud)

Heroku(Cloud)

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

![image (5)](https://user-images.githubusercontent.com/51218875/155870084-ddeb3b0b-79d8-4b81-b6bc-f067c8267c3e.png)
![image (6)](https://user-images.githubusercontent.com/51218875/155870089-22072bd8-314b-4f21-94c6-dbdc163969b1.png)
![TSNE](https://user-images.githubusercontent.com/51218875/155870116-9dbd1376-55f9-4991-ad73-3490bec78b06.PNG)



Splitting Data into Training and Test Sets

**Model Building & Evaluation**

Comparision of Various Models After Modelling
AUC scores for Random Forest ,Decision tree & Adaboost are more when compared to other models. We can see that almost all the models performed more or less good.Random Forest model with hyperparameter tuning gave the best score out of all the models on both train and test data(Sensitivity).Eventually after observing all the model algorithm performance scores , we choose Decision tree model for deployment purpose rather than random forest because it requires low computation, thus reducing time to implement.

![image](https://user-images.githubusercontent.com/51218875/155869211-e174d425-d3b9-4776-8645-645759f7a758.png)


**ModelDeployment & Productionization**


**Local Box deployment using Flask**

**Prerequisites** : Flask file,packages,Html file,Model.pklfiles,Sublime,Anaconda Prompt

For our local deployment we need to build a model and set our project deployment folder ready which consists of an app.py (Flask file),
index.html and also store the model and key model related supporting pickle files 

![image (1)](https://user-images.githubusercontent.com/51218875/155869271-5bdbad38-9fb4-4fcb-9e7c-00bcec47de28.png)
![image (2)](https://user-images.githubusercontent.com/51218875/155869277-6d94677c-c52b-4993-b92b-96df2a2db61b.png)


**Flask Error Handling using Html**
We can handle our application errors by identifying what error code it is redirecting and handle it by adding it in our flask code and rendering a new error handler html page.

Case1: Giving Nan in an input field which is not in range 

Case 2: Leaving a field as Blank

![Nullvalues](https://user-images.githubusercontent.com/51218875/155869416-90a72dbc-2ab2-4ffc-ae54-6cdcc40bcf76.png)
![fillinvalues](https://user-images.githubusercontent.com/51218875/155869493-a1cbb92d-ee45-4551-b729-52db83cbd3b0.PNG)

**Deploy an ML Model In Cloud Using Flask APIs on AWS**
Steps:

1)Build a model on your local box (Red_hat) and store the model and other key model(Decision Tree) related variables in .pkl files

2)Launch a micro instance on AWS.

3)Connect to the AWS box [ssh]

4)Move the files to an AWS EC2 instance/box [scp]

5)Install all packages needed on the AWS box.

6)Run app.py on the AWS box.

7)Check the output in the browser


![aws](https://user-images.githubusercontent.com/51218875/155869519-d9713e43-7ecb-413e-98e2-1dc9ad03a0cd.PNG)

**Deploy an ML Model In Cloud Using Flask APIs on Heroku**

Steps:

1)Train our Model : Decision tree pkl file

2)Create Webapp using Flask and reate a requirements.txt

3)Commit the code in Github and also create a Procfile

4)Create an account in Heroku(PAAS)

5)Link the Github( to Heroku)

6)Deploy the Model on heroku (PAAS)

7)Web App is ready


![heroku](https://user-images.githubusercontent.com/51218875/155869523-001178e9-d698-4106-87ca-7a7844ac4922.PNG)


**Architecture Diagram**
The following flow chart shows the overview of the implementation process for creating a binary classification model
![architectture](https://user-images.githubusercontent.com/51218875/155869524-9b2a99f4-513f-493b-a413-57f78f3cc32e.PNG)


**References**

**Blog**:https://hackernoon.com/preview/Wpo7nThkDmzEQzHbi7rh

https://www.redhat.com/en/about https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4356897/ 

https://www.analyticsvidhya.com/blog/2020/06/auc-roc-curve-machine-learning/

https://nbviewer.org/github/ethen8181/machine-learning/blob/master/model_selection/auc/auc.ipynb

https://machinelearningmastery.com/assessing-comparing-classifier-performance-roc-curves-2/

https://medium.com/geekculture/prediction-for-redhat-business-value-6a714df469ac





