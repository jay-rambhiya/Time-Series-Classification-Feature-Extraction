# Time Series Classification and Feature Extraction for Human Activity Recognition

This project involves classifying human activities based on time series data obtained from a wireless sensor network. The dataset includes multiple activities, with each activity represented by six time series. This project covers feature extraction, confidence interval estimation, and initial steps in time series classification as part of Homework 3 for the DSCI 552 course.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Feature Extraction](#feature-extraction)
- [Binary and Multiclass Classification](#binary-and-multiclass-classification)
- [Requirements](#requirements)

## Project Overview
The primary objectives of this project are:
1. Extracting meaningful time-domain features from time series data.
2. Estimating confidence intervals for feature variances.
3. Preparing for binary and multiclass classification tasks to identify human activities.

## Dataset
The dataset is the AReM (Activity Recognition system based on Multisensor data fusion) data from the UCI Machine Learning Repository. It contains:
- Seven folders, each representing a distinct human activity.
- Six time series per activity instance:
  - `avg rss12`, `var rss12`
  - `avg rss13`, `var rss13`
  - `avg rss23`, `var rss23`

Each time series has 480 consecutive values. [Dataset Link](https://archive.ics.uci.edu/ml/datasets/Activity+Recognition+system+based+on+Multisensor+data+fusion)

## Feature Extraction
1. **Time-Domain Features**: Extracted features include:
   - Minimum, Maximum, Mean, Median, Standard Deviation, First Quartile, and Third Quartile.
   - These features are computed for each of the six time series, forming a new dataset for analysis.

2. **Confidence Interval Estimation**:
   - For each feature, the standard deviation is estimated, and a 90% bootstrap confidence interval is calculated.

3. **Feature Selection**:
   - Based on domain knowledge and statistical relevance, three primary features (e.g., Min, Mean, Max) are selected for further analysis.

## Binary and Multiclass Classification
Part 2 of this project involves training classification models:
1. **Binary Classification**:
   - Logistic regression is used to distinguish "bending" activities from other activities, involving recursive feature elimination, p-values, and L1-penalized logistic regression.

2. **Multiclass Classification**:
   - L1-penalized multinomial regression and Naïve Bayes models are trained to classify multiple activities, with model performance evaluated via confusion matrices and ROC curves.

## Requirements
The project requires:
- Python
- Libraries: `numpy`, `pandas`, `scipy`, `matplotlib`, `sklearn`
