# Conversion Rate Challenge

Supervised machine learning project developed during **Bloc 3** of the CDSD (Concepteur Développeur en Science des Données) training program.
The objective of the project is to predict whether a user will subscribe to the *Data Science Weekly* newsletter based on a small set of behavioral and demographic features. 

The project follows the format of a machine learning competition inspired by Kaggle, where models are evaluated using an independent leaderboard and the **F1-score** metric. 

---

# Academic Context

This project was completed as part of:

**Bloc 3 — Supervised Machine Learning**

The bloc focuses on:

* supervised learning workflows
* preprocessing pipelines
* model evaluation
* hyperparameter optimization
* feature importance analysis
* business-oriented interpretation of machine learning models

The objective was not only to build a predictive model, but also to understand the drivers of user conversion behavior and provide actionable business recommendations.

---

# Project Objective

The company behind the project is:

**Data Science Weekly**

A newsletter platform where users can subscribe to receive weekly curated content related to data science and machine learning. 

The goal of the project is to predict whether a user visiting the website will subscribe to the newsletter using features such as:

* age
* country
* traffic source
* browsing behavior
* visitor status

The project also aims to identify which features most influence conversion probability in order to improve the newsletter conversion rate.

---

# Repository Structure

```text
.
├── data
│   ├── conversion_data_train.csv
│   ├── conversion_data_test.csv
│   │
│   └── logs
│       └── model_logs.csv
│
├── notebooks
│   ├── EDA.ipynb
│   ├── Random_forest.ipynb
│   └── XGBoost.ipynb
│
├── recommendations.md
├── requirements.txt
└── README.md
```

---

# Dataset

The project uses two datasets:

## Training Dataset

```text
conversion_data_train.csv
```

This dataset contains:

* explanatory variables (`X`)
* target variable (`converted`)

It is used to:

* perform EDA
* preprocess the data
* train machine learning models
* evaluate performances

---

## Test Dataset

```text
conversion_data_test.csv
```

This dataset contains only explanatory variables and is used to:

* generate final predictions
* create leaderboard submissions

---

# Project Workflow

## 1. Exploratory Data Analysis

Notebook:

```python
EDA.ipynb
```

This notebook focuses on:

* dataset exploration
* missing value inspection
* duplicate checks
* target distribution analysis
* visualization of important variables
* preprocessing preparation

Several visualizations were created to better understand conversion patterns and user behavior.

---

## 2. Random Forest Model

Notebook:

```python
Random_forest.ipynb
```

This notebook contains:

* preprocessing pipelines
* train/test split
* Random Forest training
* hyperparameter optimization
* model evaluation
* confusion matrix analysis
* feature importance interpretation

The Random Forest model achieved strong predictive performance and highlighted the importance of user engagement variables.

---

## 3. XGBoost Model

Notebook:

```python
XGBoost.ipynb
```

This notebook contains the final optimized model used for leaderboard submission.

Main steps:

* preprocessing with pipelines
* hyperparameter tuning using GridSearchCV
* model evaluation with F1-score
* feature importance analysis
* submission generation

XGBoost achieved the best overall performance among the tested models. 

---

# Models Tested

The project experimented with several supervised learning models:

* Logistic Regression
* Random Forest
* XGBoost

The final selected model was:

## XGBoost

because it achieved the best balance between:

* precision
* recall
* F1-score

The model was particularly effective at handling non-linear relationships and interactions between variables. 

---

# Evaluation Metric

The competition metric is:

## F1-score

The F1-score is appropriate because the dataset is imbalanced, meaning converted users represent a minority of observations. 

The project also evaluates:

* precision
* recall
* ROC-AUC
* confusion matrices

---

# Feature Importance Analysis

The analysis of feature importance showed that the most influential variable is:

* `total_pages_visited`

This indicates that user engagement strongly impacts newsletter subscription probability. Users who browse more pages are significantly more likely to convert.

Other important variables include:

* `country`
* `new_user`
* `age`
* `source`

The analysis helped identify behavioral patterns linked to conversions and provided actionable insights for improving marketing strategies. 

---

# Business Recommendations

Based on the final model analysis, several recommendations were identified:

* improve website engagement
* encourage users to visit more pages
* optimize onboarding for new visitors
* personalize campaigns depending on the country
* focus marketing efforts on high-performing acquisition channels

The model could also be used in production to identify users with a high probability of conversion and target them with personalized marketing actions.

---

# Technologies Used

* Python 3.11
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* XGBoost
* Plotly
* Jupyter Notebook

Dependencies are listed in:

```text
requirements.txt
```



---

# Installation

Clone the repository:

```bash
git clone <repository-url>
cd Bloc_03_Conversion_rate_2026
```

Create and activate a virtual environment:

```bash
python3.11 -m venv env_conversion_3_11
source env_conversion_3_11/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

---

# Outputs

Main outputs of the project:

* exploratory data analysis notebooks
* trained machine learning models
* leaderboard submission files
* feature importance visualizations
* business recommendations

---

# Conclusion

This project demonstrates that machine learning models can effectively predict newsletter subscription behavior using a limited set of user features.

Among the evaluated models, XGBoost achieved the best overall performance and was selected as the final model. The analysis also highlighted the strong importance of user engagement variables, especially the number of visited pages.

The project shows how predictive modeling can help businesses better understand user behavior and improve conversion strategies through data-driven decisions.
