# Predictive model to analyze ‘Responsiveness of customers to Starbucks offers’
![Alt text](https://www.bakingbusiness.com/ext/resources/2019/4/04292019/StarbucksRewardsApp_Lead.jpg?1556306856=true "Starbucks-Capstone-Project")
In this project, I have analyzed customer behavior in the Starbucks mobile app. The customers receive promotional offers every few days. The task is to identify which customers are influenced by promotional offers. From a business perspective, it doesn’t make sense to send all offers to all customers and this analysis will help us find target audience in order to optimize marketing ROI.
## Installation
For running this project, the most important library is Python 3 version of Anaconda Distribution. It installs all necessary packages for analysis and building models. Additionaly, you will need to install 'progressbar2' package.
## Introducing the datasets
The dataset is in 3 files. 
  1. portfolio.json — containing offer ids and meta data about each offer (duration, type, etc.)
  2. profile.json — demographic data for each customer
  3. transcript.json — records for transactions, offers received, offers viewed, and offers completed
## File Description
### Readme
This file provides high level overview of the work done in project.
### data
1. Three data files provided by Starbucks (explained in dataset introduction)
2. combined_data.csv which saves combined version of the above three files
### Starbucks_Capstone_notebook.ipynb
Code for analysis and results visualization
### Starbucks_Capstone_notebook.html
HTML version of the code
## Project Motivation
With this project, I would like to solve the following problems:
1. Predict whether or not a customer will respond to an offer.
2. Identify the most important features for the above prediction.
## Data Preparation
The cleaning stage includes: converting categorical columns to binary columns, removing outliers. missing data, cleaning date and time formats, extracting values from a dict column into separate columns.
The preprocessing stage includes: separating transactions and offers data, combining offer portfolio, customer profile, and transaction data.
## Modeling
Modeling stage includes: 
1. Finding out the accuracy and F1-score of a naive predictor model that assumes all offers were successful. 
2. Buidling and comparing performance of a logistic regression and random forest model. 
3. Optimizing the best performing model through parameter tuning.
4. Finding out most important features in these predictions.
## Results
1. Random forest model has the best training data and test data accuracy and F1-score: 
  * Training data:
    * RandomForestClassifier model accuracy: 0.761
    * RandomForestClassifier model f1-score: 0.752 
  * Test Data:
    * RandomForestClassifier model accuracy: 0.738
    * RandomForestClassifier model f1-score: 0.729
2. The top 5 features that play most important role in the predictions are:
    1. Mobile channel as medium of offer
    2. Age of the customer
    3. Social platform as medium of offer
    4. Reward amount
    5. The year a person became Starbucks member
## Blog Post
The main observations of the analysis are published here: [on medium.com](https://medium.com/starbucks-capstone-project/introduction-490213b1f474)
## Acknowledgement
Thanks to Udacity Data Scientist Nanodegree content creators for providing us the opportunity to work on this project and Starbucks for providing the dataset.
