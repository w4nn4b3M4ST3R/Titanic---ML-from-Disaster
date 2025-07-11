# 🚢 Titanic Disaster Prediction with Machine Learning

This project aims to predict passenger survival on the Titanic using classic machine learning techniques. Through systematic data loading, feature classification, exploratory analysis, feature engineering, data wrangling, and baseline model comparison, we identify the factors most critical to survival and build predictive models. 🌟

---

## 📑 Table of Contents

- 📋 [Project Overview](#project-overview)  
- 🗂️ [Dataset Description](#dataset-description)  
- 📥 [Loading Data](#loading-data)  
- 🧩 [Feature Classification](#feature-classification)  
- 🔍 [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)  
- 🛠️ [Feature Engineering](#feature-engineering)  
- 🧹 [Data Wrangling](#data-wrangling)  
- 🤖 [Baseline Model Comparison](#baseline-model-comparison)  
- 🏁 [Results & Conclusion](#results--conclusion)  
- ✉️ [Contact & References](#contact--references)  

---

## 🚀 Project Overview

The Titanic Disaster Prediction project leverages passenger manifest data to forecast survival outcomes. By examining variables such as age, gender, class, and fare, we construct a pipeline that:

- 🧐 Ingests and inspects raw data  
- 📂 Categorizes features by type and importance  
- 📈 Performs visual and statistical exploratory analysis  
- ✨ Crafts new predictive features  
- 🧼 Cleans, encodes, and scales inputs  
- 📊 Benchmarks various machine learning models  

---

## 🗂️ Dataset Description

We work with the official **Kaggle Titanic - Machine Learning from Disaster** dataset:

- **train.csv**: 891 labeled records (PassengerId, Survived, Pclass, Name, Sex, Age, SibSp, Parch, Ticket, Fare, Cabin, Embarked)  
- **test.csv**: 418 unlabeled records for final submission  
- **gender_submission.csv**: Example format for predictions  

---

## 📥 Loading Data

Load the CSV files and inspect their shape & preview

## 🔖 Feature Classification

* **Numeric:**	          `Age`, `Fare`, `SibSp`, `Parch`

* **Categorical:**	      `Survived (target)`, `Pclass`, `Sex`, `Embarked`, `Cabin`

* **Text / Identifier:**  `Name`, `Ticket`

## 🔍 Exploratory Data Analysis (EDA)

* ✅ Check missing values and basic statistics

* 📊 Visualize distributions: Age, Fare, SibSp/Parch

* 📈 Analyze survival rates by Sex, Pclass, Embarked

* 🗜️ Detect outliers via boxplots

## 🛠️ Feature Engineering

* 👪 Create FamilySize = SibSp + Parch + 1

* 🏷️ Define IsAlone flag for single passengers

* 🎩 Extract Title from Name (Mr, Mrs, Miss, etc.)

* 🏠 Group Cabin by first letter, fill missing as ‘U’ (Unknown)

* 🔢 Encode categorical variables (One-Hot / Label Encoding)

## 🧹 Data Wrangling
* 🩹 Impute missing Age by median of each Title group

* 🛟 Fill missing Embarked with mode

* 💵 Fill missing Fare by median of Pclass

* 📏 Scale numeric features using StandardScaler

## 🤖 Baseline Model Comparison

### Evaluate classifiers using 5-fold cross-validation on accuracy

## 🏁 Results & Conclusion
* ###  📊 Visualize Mean and Standard Deviation of each model
* ###  🏆 The *summary table* of mean accuracy and standard deviation for all baseline models

## ▶️ How to Run
* 1. Create and activate a virtual environment *(recommended)*
    ``` bash
    python3 -m venv venv
    # macOS / Linux
    source venv/bin/activate
    # Windows (PowerShell)
    .\venv\Scripts\Activate.ps1
    ```
* 2. Install dependencies
    ``` bash
    pip install --upgrade pip
    pip install -r requirements.txt
    ```
* 3. Launch the analysis *(recommended: use Jupyter Notebooks for the best experience.)*
    ``` bash
    jupyter notebook
    ```