# Online Toxicity Analysis: Comparative Evaluation of Text Classification and Topic Modeling Techniques

## Project Overview
This project applies text mining techniques to classify and analyze toxic comments from the ["Toxic Comment Classification Challenge" dataset](https://www.kaggle.com/competitions/jigsaw-toxic-comment-classification-challenge/). The project is divided into two main tasks:

1. **Text Classification** (detecting various types of toxicity).
2. **Topic Modeling** (analyzing underlying themes in toxic and identity-hate comments).

For a detailed explanation of the methodology, results, and conclusions, please refer to the project documentation:
* **[Project Report (PDF)](report/Text_Mining_Report.pdf)**
* **[Presentation Slides (PDF)](report/Text_Mining_Presentation.pdf)**
* **[Presentation Slides (PPTX)](report/Text_Mining_Presentation.pptx)**

## Directory Structure
```text
Toxic_Comment_Classification/
├── notebooks/                             # Jupyter notebooks for analysis
│   ├── Toxic_Comment_Classification.ipynb # Main classification pipeline
│   ├── Toxic_Comment_Topic_Modeling.ipynb # Topic modeling on general toxicity
│   └── Identity_Hate_Topic_Modeling.ipynb # Topic modeling on identity hate
│
├── report/                                # Project documentation
│   ├── Text_Mining_Presentation.pdf       # Project presentation (PDF)
│   ├── Text_Mining_Presentation.pptx      # Project presentation (PPTX)
│   └── Text_Mining_Report.pdf             # Project report
│
├── requirements.txt                       # Required Python libraries  

```

---

## Installation and Setup

### Prerequisites

* Python
* Google Colab environment (preferred) or Jupyter Notebook

### Required Libraries

To run the notebooks in a local setup, simply install the dependencies from the requirements file:

```bash
pip install -r requirements.txt
```

### Models

You can access the trained models via the following [Google Drive folder](https://drive.google.com/drive/folders/1Pa-fyxohtwRcoJExOtYnRjEdfi52b1GO?usp=sharing).

### Dataset

The notebooks are configured to download the dataset (`jigsaw-toxic-comment-classification-challenge.zip`) directly from Google Drive.

---

## Part 1: Text Classification

### Notebook

`notebooks/Toxic_Comment_Classification.ipynb`

### Description

This notebook performs the supervised learning tasks. It includes:

* **Data Preprocessing:** Cleaning text, tokenization, lemmatization, and stopword removal.
* **Exploratory Data Analysis (EDA):** Visualization of label distribution and word clouds.
* **Model Training & Evaluation:**
* *Traditional ML:* Logistic Regression, Naive Bayes, and Linear SVM using TF-IDF.
* *Deep Learning:* Fine-tuning a DistilBERT transformer model.



### Instructions

1. Open `Toxic_Comment_Classification.ipynb`.
2. Run the cells sequentially. The data will automatically download to a `data/` folder.
3. The notebook evaluates models using **ROC-AUC** and **F1 scores**.
4. Saved models corresponding to this section are expected to be located in `models/ML_model` (Logistic Regression) and `models/DistilBERT_model`.

---

## Part 2: Topic Modeling

### Notebooks

1. `notebooks/Toxic_Comment_Topic_Modeling.ipynb`
2. `notebooks/Identity_Hate_Topic_Modeling.ipynb`

### Description

These notebooks use unsupervised learning to discover abstract topics within the comments.

* `Toxic_Comment_Topic_Modeling.ipynb`: Applies **LDA** and **BERTopic** to comments labeled as 'toxic'.
* `Identity_Hate_Topic_Modeling.ipynb`: Focuses specifically on the 'identity_hate' category to understand targeted hate speech patterns.

### Instructions

1. Open the desired notebook.
2. Ensure `bertopic` and `gensim` are installed (cells included in the notebook).
3. Run the cells to process the text and generate topic clusters.
4. The notebooks provide visualizations to get insights.
