# Credit Card Fraud Recognition Through Autoencoders and Random Forests
This was my capston project for the Machine Learning Engineer Nanodegree Program at Udacity. If you are interested, you can read both the `proposal.pdf` and `report.pdf` that explain in more detail the project.

## Project Overview
As reported by BusinessInsider, last year, CreditCards.com found that credit card fraud was on the rise. Both number of frauds and types of credit card scams are more and more. These numbers seem unfortunately destined to grow even more in the future. For this reason, it is important to find a way to automatically recognise anomalies.
A lot of research has been done in order to find a solution to this problem. 

## Problem Statement
The aim of the fraud detection system is to detect fraud accurately and before fraud is com- mitted. The goal is to detect least and accurate false fraud detection. The most commonly techniques used fraud detection methods are Nave Bayes (NB), Support Vector Machines (SVM) and K-Nearest Neighbor algorithms (KNN). Each transaction has a set of unique features, such as the value of the transaction, the time at which it occured, issuer and recipient, an id and other sensitive data. The problem will be structured as a classification problem, where each transaction could be classified as ”Normal” or ”Fraud”.

## Datasets and Inputs
In order to reproduce this kind of problem, I found a useful dataset available on Kaggle (https://www.kaggle.com/mlg-ulb/creditcardfraud). The datasets contains transactions made by credit cards in September 2013 by european cardholders. This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced and the positive class (frauds) account for 0.172% of all transactions.
It contains only numerical input variables which are the result of a PCA transformation. Due to confidentiality issues, the authors cannot provide the original features and more background information about the data. Features V1, V2, ... V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are ”Time” and ”Amount”. Feature ”Time” contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature ”Amount” is the transaction Amount, this feature can be used for example-dependant cost-senstive learning. Feature ”Class” is the response variable and it takes value 1 in case of fraud and 0 otherwise.

## Solution Statement
The aim of this project was to measure the results of an autoencoder with a most established model, random forests. The neural network has been developed with `Keras`, while the random forest uses `sklearn`. The data has been augmented with `imblearn` in order to balance the two classes.

## Run the Implementation
You can execute the code following thise steps:
1. Open the `AutoencodersCreditCardFraudsDetection.ipynb`
2. Install all the libraries that are imported in the first block of code;
3. Run each block.
