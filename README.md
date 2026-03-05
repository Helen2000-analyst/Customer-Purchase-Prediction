# Online Shoppers Customer Intention Prediction

### About Dataset
This dataset was sourced from kaggle. It contains 18 columns and 12,330 rows.

### Project Overview
This project analyzes online shopping behavior and builds machine learning models to predict whether a website visitor will generate revenue (make a purchase) during a browsing session. Understanding purchase intent can help businesses improve marketing strategies, personalize user experiences, and increase conversion rates.

The goal of this project was to develop a predictive model that accurately identifies customers who are more likely to complete a purchase based on their browsing behavior.

### Business Problem

E-commerce platforms receive thousands of visitors daily, but only a small percentage complete a purchase. Businesses need a way to identify high-intent visitors in order to:

 - Improve targeted marketing
 - Optimize advertising spend
 - Personalize user experiences
 - Increase conversion rates

This project uses historical user session data to predict purchase behavior.

### Dataset

The dataset used is the  <a href=  "https://www.kaggle.com/datasets/imakash3011/online-shoppers-purchasing-intention-dataset">Online Shoppers Purchasing Intention Dataset</a> which contains session-based information about visitors on an e-commerce website.

Key features include:
 - Administrative pages visited
 - Product-related pages
 - Bounce rate
 - Exit rate
 - Page value
 - Traffic type
 - Visitor type
 - Month of visit

The target variable is:

### Revenue

 - 0 → No purchase

 - 1 → Purchase made

The target variable is:

### Project Workflow
1. Data Cleaning

 - Loaded the dataset using Pandas
 - Checked for missing values
 - Converted categorical variables to numerical values
 - Encoded categorical columns

2. Exploratory Data Analysis
EDA was performed to understand user behavior patterns.

### Correlation Heatmap

<img width="846" height="621" alt="Screenshot (821)" src="https://github.com/user-attachments/assets/b03ddbc1-2db8-4554-829f-8db478b2289c" />

Using Seaborn

     i bash
     
     ii conda install seaborn

     

 and Matplotlib,

      i bash
      
      ii pip install matplotlib

 
 
 
 several visualizations were created to understand patterns in user behavior:

 - Correlation heatmaps

 - Feature distribution analysis

 - Visitor behavior patterns



