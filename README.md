# Email-Spam-Detection-Using-NLP

An end-to-end Machine Learning pipeline to classify emails as **Spam** or **Ham** (not spam) using Natural Language Processing (NLP) and scikit-learn.

## 📊 Project Overview

This project implements a text classification model that processes raw email text, extracts features using TF-IDF, and trains a Random Forest classifier to accurately detect spam messages.

### Key Results (Test Set)
* **Accuracy**: 0.9836 (98.36%)[cite: 1]
* **Training Data**: 9,248 emails[cite: 1]
* **Test Data**: 2,313 emails[cite: 1]
* **Duplicates Removed**: 439 duplicated emails were cleaned from the dataset[cite: 1]

## 🛠️ Tech Stack

* **Python**
* **Pandas** for data manipulation[cite: 1]
* **Scikit-learn** for machine learning models and pipelines[cite: 1]:
  * `TfidfVectorizer` (with English stop words removal)[cite: 1]
  * `RandomForestClassifier` (100 estimators)[cite: 1]
  * `Pipeline` for seamless workflow integration[cite: 1]

## 📋 Dataset Preparation

1. **Loading & Cleaning**: Loads data from `emails.csv`, drops missing values in `text` and `label` columns, and converts spam labels to binary format (`1` for spam, `0` otherwise)[cite: 1].
2. **Deduplication**: Identifies and removes duplicate email texts to prevent data leakage (439 duplicate emails removed)[cite: 1].
3. **Stratified Split**: Splits the dataset into 80% training data and 20% test data, maintaining class proportions using stratification (`random_state=42`)[cite: 1].

## 🚀 Model Evaluation

The model was evaluated on the test set (2,313 emails), achieving strong performance across metrics nicluded in the confussion matrix.

