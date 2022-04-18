# Bankruptcy-Prediction
Using classification model in R, predicting if the company will go bankrupt or not

## Objective
The objective of the project is to use the features (i.e., financial parameters) given in the dataset to understand their impact in identifying whether a company will face bankruptcy in the future or not.

## Business Understanding
Firm Description

**CTBC BANK**
 
 •  Established in 1966 is one of the largest private banks in Taiwan, headquartered in Taipei.

**Number of Employees**

 •  11,000 employees

**Geographic Footprint of the Firm**

 •  152 branches in Taiwan
 •  116 overseas branches across 14 countries such as the US, Canada, Japan, Indonesia, the Philippines, India, Thailand, Vietnam, Malaysia, Hong Kong, Singapore, China, Myanmar, and Australia.

**Major Product or Service Line**

 •  Institutional banking, capital markets, and overseas business
 •  Retail banking

**Revenues tied to each Product or Service line**

<img width="468" alt="image" src="https://user-images.githubusercontent.com/58331935/163730453-69fed42f-40d3-4734-9f0d-b129b6322b03.png">

**Line of business that is the subject of Analysis**

 •  Retail Banking- Loan services:
 
Small and medium-sized enterprises are provided with diverse loan services including land loan, factory loan, loan for purchase of machinery and equipment,  refinancing, installment loans, policy-based loans, financial planning mortgages, unsecured term loans, and revolving loans, export loan, purchase turnover financing.

 •  Global Risk Management Group:
 
Responsible for regulatory compliance such as Credit Risk Management.  This includes maintenance of minimum regulatory capital as per central bank regulations and submitting reports for the same.

**SWOT Analysis**

<img width="468" alt="image" src="https://user-images.githubusercontent.com/58331935/163730543-8193f4ef-ce5c-434a-b5e1-6ab8c31bb81c.png">
 
## Data Description

Dataset is from UCI Machine
Learning Repository: https://archive.ics.uci.edu/ml/datasets/Taiwanese+Bankruptcy+Prediction

Deron Liang and Chih-Fong Tsai, deronliang'@'gmail.com; cftsai'@’mgt.ncu.edu.tw, National Central University, Taiwan Company bankruptcy was defined based on the business regulations of the Taiwan Stock Exchange.

The data is collected from the Taiwan Economic Journal for the years 1999 to 2009

## Data Analysis and Understanding

Number of records:                      6819
Number of features/ variables:    96
Target variable of interest:            Bankrupt?
 
## Dataset Fields and Description
 
![image](https://user-images.githubusercontent.com/58331935/163730574-91c02158-09e5-41cb-8d0f-e641835c6929.png)

![image](https://user-images.githubusercontent.com/58331935/163730583-434bbcca-d5e2-4157-8576-68fc6c834dfb.png)

**Dataset Fields and Description**
 
 ![image](https://user-images.githubusercontent.com/58331935/163730595-4c67f14d-e866-49cb-8934-4341fc6f9843.png)

 ![image](https://user-images.githubusercontent.com/58331935/163730626-f496a9de-f6e4-4b0d-8198-37eb95e0c094.png)

 ![image](https://user-images.githubusercontent.com/58331935/163730664-0f0598a1-5f17-498f-bb6e-42fad3216bdf.png)
 
 ![image](https://user-images.githubusercontent.com/58331935/163730667-608c3cb7-3423-4efc-8ab6-de134cb17ccd.png)
 
## Summarize the dataset

**Target Variable Distribution**

 •  We can observe that our dataset is very imbalanced. 
 •  The minority class which is the one we're most interested by predicting represents about 3% of total observations.  
 
![image](https://user-images.githubusercontent.com/58331935/163730758-c8ca9527-fe96-4e2e-937b-dc34da894d5c.png)
 
**Target variable correlation**

![image](https://user-images.githubusercontent.com/58331935/163730779-ba017528-6688-4d1c-ade3-70a727f62dd1.png)
 
**Correlation Matrix**

 •  One thing to point out is that there are groups of features that appear highly correlated with each other as well as the label. 
 
![image](https://user-images.githubusercontent.com/58331935/163730790-ca491068-8a7d-4a2e-8a6e-6d868eac604e.png)

**Data Statistics**

![image](https://user-images.githubusercontent.com/58331935/163730870-d56afeed-31fc-47dd-8821-18d650cdf39c.png)

**Histograms**
 
![image](https://user-images.githubusercontent.com/58331935/163730877-e68d2068-8db1-4152-bf75-752da3edac3b.png)
 
**Boxplots**

 •  Major values are concentrated around starting ranges yet there are very high valued records.
 •  Some features show outliers in top 1% values only. Few of such features are: Total_debt/Total_net_worth Revenue_per_person Net_Value_Growth_Rate Revenue_Per_Share etc
 •  There are some features that have significant number of higher values, like: Current_Asset_Turnover_Rate Cash_Turnover_Rate

![image](https://user-images.githubusercontent.com/58331935/163730898-44d62f3f-09e5-44c1-96ef-1e4c05c5be29.png)
![image](https://user-images.githubusercontent.com/58331935/163733135-661d2ce8-d28d-4b87-b118-cc1fb8567796.png)

## Data Modeling

**Prediction:**

To predict if a company will go bankrupt or not.

**Hope to Accomplish:**

We hope to build a classification model that will predict the bankruptcy and help lenders, shareholders and investors to make informed decisions.
Target variable Description: Bankrupt? 
Target variable determines if a company is bankrupt or not. 1 - bankrupt 0 - not bankrupt

**Classification models:**

Decision Trees

Random Forest Classifier

Logistic Regression

**Data Transformation: Each model is run with the following.**

Original data

Scaled data

SMOTE

**Analysis of metrices such as accuracy, confusion matrix to determine the best model for the prediction.**

**Data Split:**

![image](https://user-images.githubusercontent.com/58331935/163731148-d7f4335f-bb32-4d57-addf-6644cd531a5a.png)
 
**Number of Missing Values : 0**

![image](https://user-images.githubusercontent.com/58331935/163731178-0f3992e6-a7ed-42d7-891c-c2ef2bbfc75d.png)
 
## Logistic Regression Model

**Summary Statistics**

![image](https://user-images.githubusercontent.com/58331935/163731204-3318d374-0c1d-4e48-991d-9c8597649f06.png)
 
**ROC Curve**

![image](https://user-images.githubusercontent.com/58331935/163731244-fa3156fc-e178-4cbb-a8dc-6a2261cf6455.png)
 
## Decision Tree Model (Scaled Data)

TRANSFORMATION: Scaling Max-depth: 30

**Decision Tree**

![image](https://user-images.githubusercontent.com/58331935/163731346-3afeb02b-3b43-4f80-b3fe-370d1be2da0b.png)
 
**Summary Statistics**

![image](https://user-images.githubusercontent.com/58331935/163731355-29270c7a-5992-47f5-a2eb-92fed61cf038.png)
 
**ROC Curve**

![image](https://user-images.githubusercontent.com/58331935/163731361-03a38bdf-66f8-48d2-b5c1-ce16a7181145.png)

## Random Forest Model (SMOTE)

Transformation: SMOTE algorithm for unbalanced classification problems
This function handles unbalanced classification problems using the SMOTE method. 

**SMOTE Dataset**

![image](https://user-images.githubusercontent.com/58331935/163731377-06e6464a-cf28-411b-aa48-5516a8bd9809.png)

**Target Variable Distribution (SMOTE Dataset)**

![image](https://user-images.githubusercontent.com/58331935/163731382-f378f9af-b9be-45ea-b932-75cb014c6def.png)
 
**Summary Statistics**

![image](https://user-images.githubusercontent.com/58331935/163731394-e9a39b04-f041-4b42-befb-1ab5d88d5a82.png)
 
**ROC Curve**

![image](https://user-images.githubusercontent.com/58331935/163731421-cf77d120-eab8-4da5-a469-a596c607b3c2.png)
 
## Model Performance Comparison

**ROC Curves**

 ![image](https://user-images.githubusercontent.com/58331935/163731753-e9c1bbc9-958a-458a-8088-9fdbd16ac877.png)
 
**Model Performance Metrices**

 ![image](https://user-images.githubusercontent.com/58331935/163731767-38f62640-03ec-434b-bcf3-ba25a0c2a643.png)

**Final Model** LOGISTIC REGRESSION

## Prediction with Test data using Logistic Regression (Final Model)

**Summary Statistics**

 ![image](https://user-images.githubusercontent.com/58331935/163731786-56115529-2659-48ba-9510-618dc05837dc.png)
 
**ROC Curve**

 ![image](https://user-images.githubusercontent.com/58331935/163731793-67016128-8beb-43e0-ae8c-31dbe6ce7b9b.png)
 
**Variable Importance Plot**

 ![image](https://user-images.githubusercontent.com/58331935/163731798-6d2603c9-c712-40bf-b7a1-42e401e9ad37.png)

## Limitations

 •  Most companies tend to submit flawed statements or are limited by the availability
 •  Assumption that the models are stable across economic conditions that change over time, such as inflation, interest rates, and credit availability
 •  The companies which gets predicted as bankrupt by the model but is not actually bankrupt leads to loss of potential business and thereby profits for the bank
 •  The companies which are classified as not bankrupt by the model but are bankrupt lead to risk of default for the bank
 
## Improvement Scope

 •  The data contains outliers in almost all the variables. Corrective measures in each one of them can drive increased performance of the model.
 •  Other classification algorithms such as K-nearest neighbours, Naive Bayes, SVM etc
 •  More accurate predictions can be made from separate industry-based models
 •  Factor the current macroeconomic conditions like growth rates, inflation, and interest rates into the model
 
## Recommendations
**CTBC Bank can use this model to evaluate a company’s financial stability before establishing new relationships or engagements with a company.**

 ![image](https://user-images.githubusercontent.com/58331935/163731872-2ebfbaf9-5c7c-4c28-958b-d7825ac521dd.png)
 
 •  They can decide if the loan requested by a company should be sanctioned or not depending on if it classifies as bankrupt or not by the model. 
 •  Furthermore, this model can also be used to set interest rates for the loan issued. 
 •  For example, if a company gets classified as bankrupt by the model and CTBC still wants to sanction the loan, they can quote a higher interest rate to take into account the risk of being bankrupt and hence default of loan.
 
**CTBC Bank can also use this model to assess the financial distress of companies that they have already lend to.**

 ![image](https://user-images.githubusercontent.com/58331935/163731893-a94c97f6-7f34-4649-baa6-4f2f486b4107.png)
 
 •  The prediction of a company as bankrupt or not can be used to set aside exposure amounts which are subject to default. 
 •  This model can also be used by CTBC Bank to determine the floating interest rate for the loan which can be increased or decreased based on bankruptcy prediction.
 
**CTBC Bank can utilize this model to calculate the minimum regulatory capital required to be maintained by every bank as per Central Bank of Republic of China (Taiwan)**

 ![image](https://user-images.githubusercontent.com/58331935/163731903-b540d7ec-46e4-46e0-bd7d-a75f527d3648.png)
 
## About

Identifying whether a company will face bankruptcy in the future or not using machine learning models in R
