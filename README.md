# Toxic_Comment_Classification
Toxic comments classification from the "Jigsaw Toxic Comment Classification Challenge" dataset.

## Project Overview
This project applies text mining techniques to classify and analyze toxic comments from the "Toxic Comment Classification Challenge" dataset. The project is divided into two main tasks:
1. Text Classification (detecting various types of toxicity).
2. Topic Modeling (analyzing underlying themes in toxic and identity-hate comments).

## PART 1: TEXT CLASSIFICATION
### NOTEBOOK: Notebooks/Toxic_Comment_Classification.ipynb

This notebook performs the supervised learning tasks. It includes:
- Data Preprocessing: Cleaning text, tokenization, lemmatization, and stopword removal.
- Exploratory Data Analysis (EDA): Visualization of label distribution and word clouds.
- Model Training & Evaluation:
  - Traditional ML: Logistic Regression, Naive Bayes, and Linear SVM using TF-IDF.
  - Deep Learning: Fine-tuning a DistilBERT transformer model.

## PART 2: TOPIC MODELING
### NOTEBOOKS: 
1. Notebooks/Toxic_Comment_Topic_Modeling.ipynb
2. Notebooks/Identity_Hate_Topic_Modeling.ipynb

These notebooks use unsupervised learning to discover abstract topics within the comments.
- `Toxic_Comment_Topic_Modeling.ipynb`: Applies LDA and BERTopic to comments labeled as 'toxic'.
- `Identity_Hate_Topic_Modeling.ipynb`: Focuses specifically on the 'identity_hate' category to understand targeted hate speech patterns.
