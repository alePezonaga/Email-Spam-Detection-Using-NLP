# Email-Spam-Detection-Using-NLP

An end-to-end Machine Learning pipeline to classify emails as **Spam** or **Ham** (not spam) using Natural Language Processing (NLP) and scikit-learn.

##  Project Overview

This project implements a text classification model that processes raw email text, extracts features using TF-IDF, and trains a Random Forest classifier to accurately detect spam messages.

### Key Results (Test Set)
* **Accuracy**: 0.9836 (98.36%)
* **Training Data**: 9,248 emails
* **Test Data**: 2,313 emails
* **Duplicates Removed**: 439 duplicated emails were cleaned from the dataset

##  Tech Stack

* **Python**
* **Pandas** for data manipulation
* **Scikit-learn** for machine learning models and pipelines:
  * `TfidfVectorizer` (with English stop words removal)
  * `RandomForestClassifier` (100 estimators)
  * `Pipeline` for seamless workflow integration

##  Dataset Preparation

1. **Loading & Cleaning**: Loads data from `emails.csv`, drops missing values in `text` and `label` columns, and converts spam labels to binary format (`1` for spam, `0` otherwise).
2. **Deduplication**: Identifies and removes duplicate email texts to prevent data leakage (439 duplicate emails removed).
3. **Stratified Split**: Splits the dataset into 80% training data and 20% test data, maintaining class proportions using stratification (`random_state=42`).

##  Model Evaluation

The model was evaluated on the test set (2,313 emails), achieving strong performance across metrics nicluded in the confussion matrix.

