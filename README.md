# comparing_classifiers

## Overview: 

In this practical application, our goal is to compare the performance of the classifiers, namely K Nearest Neighbor, Logistic Regression, Decision Trees, and Support Vector Machines. We will utilize a dataset related to marketing bank products over the telephone. Our dataset comes from the UCI Machine Learning repository at [link](https://www.google.com/url?q=https%3A%2F%2Farchive.ics.uci.edu%2Fml%2Fdatasets%2Fbank%2Bmarketing). The data is from a Portuguese banking institution and is a collection of the results of multiple marketing campaigns.

## Files:

1. prompt_III.ipyb: The main Jupyter Notebook with the analysis.
2. data/bank-additional-names.txt: A description of data and the datasource.
3. data/bank-additional-full.csv: The full dataset.
4. data/bank-additional.csv: A smaller subset (approximately 1/10th) of the full dataset to be used for SVM.
5. README.md: This file

## Conclusions:
When comparing different Classifier models, we find that all models generalize well, and are close in performance, with the Decision Tree (DT) topping out on the test accuracy at 91.35% using the full dataset. Both, Linear Regression and KNN tied at 90.82% test accuracy, with only a small (~0.53%) loss in accuracy from Decision Tree.

In the small dataset SVM performed the best, however it requires higher computational resources so was not tested with the full dataset.

The business case is to lower the marketing cost and determine which customers will likely sign-up for the long-term deposit in the bank. Pre-determining good customers and calling only those that are likely to accept long-term deposit reduces the marketing expense. So a model with high accuracy, high recall and low False Negatives is ideal.

Since the dataset contains a dual-class target variable where the class distribution is highly skewed (only 11% positive-class), the business case requires us to capture most TPs, and demands low FNs. With a low recall, we shift the probability threshold to 0.17 to improve recall sacrificing accuracy.
