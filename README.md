# Project-SOEN691-BigData

# Chicago Crime Dataset 
Link: https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-present/ijzp-q8t2

# ➢ Abstract
In this project, we are going to apply Apache Spark and scikit-learn to analyze a big data set, to find valuable results behind the data. 

Crime is an inseparable part of our society. Either being a victim or an offender everybody has witnessed crime. Through this project, we will find certain trends/patterns in order to provide valuable information for the safety of society and lower crime rates. 
We have selected the “Chicago Crime dataset report” which has the incidents of crime for Chicago city that occurred from 2001 - present. 
We are going to use unsupervised and supervised machine learning techniques, including k-means Clustering, Support Vector Machine, Logistic Regression to analyze and visualize the data.


# ➢ I. Introduction

Crime is one of the most important social problems in the country, affecting public safety, children development, and adult socioeconomic status. A police officer may know where the dangerous areas  are according to his experience, but he may not be able to tell about what kind of crime could happen. Our objective is, we want to help police officers by providing useful information which is hard to get so that they can take appropriate measures. In this project, we will analyse and predict crime information as much as possible. In our study we will target following problems -

 **Exploratory Analysis:** (Graphical Analysis)
  1. During what time period of an year is the crime rate at its peak
  2. How has the crime rate changed over the years
  3. Crime hotspots in city
  
 **Predictive Analysis:**
 
  5. Predicting the type of crime based on its location
  6. Predicting the crime(s) (probability) in a particular week(holidays) for the year 2020 based on previous years.

**Related work** 
Many literatures are trying to predict the crimes. Sunil Yadav is using supervised, semi-supervised and unsupervised learning techniques to predict the crime in India, including Apriori Algorithm, Naive Bayes Algorithm and regression algorithm. Romika Yadav came up with auto regression techniques for time series data where he is trying to improve the accuracy of prediction by identifying the relationship among crimes attributes. B.Sivanagaleela is using a fuzzy C-means algorithm, but he only focuses on where the crime will occur and doesn’t care about the type of the crimes. Hongjian Wang & Team studied the problem of crime rate inference at the neighborhood level. They proposed the study of two newer types of urban data: POI and Taxi flow. POI data provides venue information such as GPS coordinates, category, popularity, and reviews and Taxi flow data reflects how people commute in the city



# ➢ II. Materials and Methods

**Dataset**

The dataset chosen for this project consists of incidents of crime reported in the city of Chicago from 2001 to 2019. Data is extracted from the Chicago Police Department's CLEAR (Citizen Law Enforcement Analysis and Reporting) system. It is one of the richest data sources in the area of crime. 
The dataset includes sufficient information about Date, Type, Description, location etc about the crime for our analysis.
 
**Approach and corresponding technologies**

In our project, we will deal with a big data set, so we need a technology that deals with big data processing efficiency. As **Spark** can do processing in-memory we will use it as our main framework. We will also implement techniques thought in class : **k-fold crossvalidation, KNN and Random Forest**.<br/>  Below is the pipeline we will follow:
 - Data Pre-Processing
 - Exploratory analysis
 - Predictive analysis 
  
  
   1\. **Data Pre-processing:**
  In this step, we will explore data, handle missing values, remove noise.
     Examples:  
    a. Implement sampling technique to overcome     
    b. Combine similar types of crimes in case of minority classes to get better predictions.

  *Technologies*: Apache Spark, pyspark Dataframe.


2. **Exploration Analysis:** 
  In this step, we will infer useful information and try to analyze important trends that will help in crime detection and  prevention. The analysis will also help identify useful features for building predictive models.

  *Methods*: Plotting graphs, pie-chart, heatmaps, querying data.
  
  *Technologies*:  pyspark DataFrame, pyspark SQL, pyspark RDD, Matplotlib, Seaborn, Folium, Tableau. 


3. **Predictive Analysis:**
  In this step, we are going to use the k-Fold Cross-Validation technique while training. We will perform the following two predictions:

    **1. Predicting the type of crime based on its location**

    To perform this prediction we will use **KNN - k nearest neighbor** to predict the type of crime that has the highest probability based on the location(latitude, longitude). The model will identify the k-nearest neighbors using Euclidean distance where k is a user-specified number. K will be decided during the implementation phase. We will also explore KNN-IS and ESkNN. 


    **2. Predicting the crime (probabilities) for a particular week(holidays) for the years 2019 and 2020**

    We will predict the type of crime that could happen during a particular week and location based on past year trends. **Random forest** methods in Spark will be used to predict the labels. K-fold cross-validation will be used to train the model for a particular week in the years from 2000 to 2018. 
    We will evaluate our model on the same week for 2019 and then predict the same for the year 2020. 
 




