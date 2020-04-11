# Project-SOEN691-BigData

# Chicago Crime Dataset 
Link: https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-present/ijzp-q8t2

# ➢ Abstract
Crime is an inseparable part of our society, either being a victim or an offender everybody has witnessed crimes. We selected the “Chicago Crime dataset report” which has the incidents of crime for Chicago city that occurred from 2001 - present. We analyzed the trends of crime over the years, locations of the crimes where it happened the most, and hotspot of crimes over the years. In our experiment, we used supervised machine learning techniques including random forest, KNN and ensemble method for the prediction of crimes based on time, location and other parameters. 


# ➢ I. Introduction

Crime is an important social problem in the country, affecting public safety, children development, and adult socioeconomic status. A police officer may know where the dangerous areas are according to his experience, but he may not be able to tell about what kind of crime could happen. Our objective is to help police officers by providing useful information which is hard to get, so that they can take appropriate measures. We have used Apache spark’s Random Forest and SciKit-learn’s KNN classifier and ensemble method for the same. Our project has below two parts -

 **Exploratory Analysis:** 
  1. Trends of the crimes over the years (2010 - 2019)
  2. Type of locations where crimes happen the most 
  3. Timelapse of crimes hotspots over the years (2010 - 2019)
  4. A brief literal sense about those crimes
  
 **Predictive Analysis:**
 
  1. Predicting the type of crime(s) and probability of crimes based on location.
  2. Predicting the type of crime(s) based on Time and also on other parameters.

**Related Work** 
Many literatures are trying to predict the crimes. Sunil Yadav et al M. Timbadia is using supervised, semi-supervised and unsupervised learning techniques to predict the crime in India, including Apriori Algorithm, Naive Bayes Algorithm and regression algorithm [1]. Romika Yadav and S. Kumari Sheoran came up with auto regression techniques for time series data where she is trying to improve the accuracy of prediction by identifying the relationship among crime attributes [2]. B.Sivanagaleela and S. Rajesh  is using a fuzzy C-means algorithm, but he only focuses on where the crime will occur and doesn’t care about the type of the crimes [3]. Hongjian Wang at el Team studied the problem of crime rate inference at the neighborhood level.



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
 
**References**

  1. S. Yadav, M. Timbadia, A. Yadav, R. Vishwakarma and N. Yadav, "Crime pattern detection, analysis & prediction," 2017 International conference of Electronics, Communication and Aerospace Technology (ICECA), Coimbatore, 2017, pp. 225-230.
  2. R. Yadav and S. Kumari Sheoran, "Crime Prediction Using Auto Regression Techniques for Time Series Data," 2018 3rd International Conference and Workshops on Recent Advances and Innovations in Engineering (ICRAIE), Jaipur, India, 2018, pp. 1-5.
  3. B. Sivanagaleela and S. Rajesh, "Crime Analysis and Prediction Using Fuzzy C-Means Algorithm," 2019 3rd International Conference on Trends in Electronics and Informatics (ICOEI), Tirunelveli, India, 2019, pp. 595-599.



