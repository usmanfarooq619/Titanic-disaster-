# Titanic-disaster
Disaster Survival Predictions
# Overview

The data has been split into two groups:

  training set (train.csv)
  test set (test.csv)

# Introduction

Problem statement : predicting survival prediction based on the given features

# Understanding the data

Train samples are 891 or 40% of the actual number of passengers on board the Titanic (2,224).
Survived is a categorical feature with 0 or 1 values.
Around 38% samples survived representative of the actual survival rate at 32%.
Most passengers (> 75%) did not travel with parents or children.
Nearly 30% of the passengers had siblings and/or spouse aboard.
Fares varied significantly with few passengers (<1%) paying as high as 512.
Few elderly passengers (<1 percent) within age range 65-80.
Names are unique across the dataset (count=unique=891)
Sex variable as two possible values with 65% male (top=male, freq=577/count=891).
Cabin values have several dupicates across samples. Alternatively several passengers shared a cabin.
Embarked takes three possible values. S port used by most passengers (top=S)
Ticket feature has high ratio (22%) of duplicate values (unique=681).


## Feature Engineering

pclass   = Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)

sex      = Sex	
Age      = Age (years)	
sibsp    = number of siblings / spouses aboard the Titanic	
parch    = number of parents / children aboard the Titanic	
ticket   = Ticket number	
fare     = Passenger fare	
cabin    = Cabin number	
embarked = Port of Embarkation	(C = Cherbourg, Q = Queenstown, S = Southampton) 
 
survival = Survival	(0 = No, 1 = Yes)


# Family Size

With the number of siblings/spouse and the number of children/parents we can create new feature called Family Size.

# Data Cleaning

converting our features into numerical values

# Feature Selection

-dropping the irrelevant features

Observations.

* Pclass=3 had most passengers, however most did not survive. Confirms our classifying assumption.
* Infant passengers in Pclass=2 and Pclass=3 mostly survived. Further qualifies our classifying assumption. 
* Most passengers in Pclass=1 survived. Confirms our classifying assumption.
* Pclass varies in terms of Age distribution of passengers.

# Modeling and Comparing

Our problem is a classification and regression problem. We want to identify relationship between output (Survived or not) with other variables or features (Gender, Age, Port...). We are also perfoming a category of machine learning which is called supervised learning as we are training our model with a given dataset. With these two criteria - Supervised Learning plus Classification and Regression, we can narrow down our choice of models to a few. These include:
* Logistic Regression
* KNN or k-Nearest Neighbors
* Support Vector Machines
* Naive Bayes classifier
* Decision Tree
* Random Forrest
* Perceptron
* Artificial neural network
* RVM or Relevance Vector Machine
