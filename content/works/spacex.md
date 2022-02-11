---
title: 'Space X Landing Prediction'
bookcase_cover_src: 'cover/cover02.png'
bookcase_cover_src_dark: 'cover/cover02.png'
weight: 10
---

# Winning Space Race with Data Science 
## Space-X Landing Prediction is an Applied Data Science Capstone Project done as part of [IBM Data Science Certification](https://www.coursera.org/account/accomplishments/professional-cert/HQZX8FQ3KAR4) Program.

### Objective
The goal of this project is to provide analysis on SpaceX launches, with focus on stage reuse and landings, to provide our company, SpaceY, competitive information on cost of launches and prediction methods on whether SpaceX will reuse a given stage.

### Methodology
* **Data collection:**
    - SpaceX API: Past landing data, plus info on boosters, cores, payloads;
    - Wikipedia scrape: Parse tables of past launches (including outcomes — success/failure) into a DataFrame for next stage.
* **Data wrangling:**
    - Outcomes (“True ASDS”, “True Ocean”, etc.) grouped into two classes — success (1) and failure (0);
    - Column ‘class’ added to DataFrame, to be used for model building and prediction.
* **Exploratory data analysis** (EDA) using Visualization and SQL:
    - Data loaded into IBM Cloud DB2 instance;
    - SQL queries run from Jupyter notebook;
    - Plotly and Seaborn; categorical plots (scatter, bar, line);
    - One-hot encoding of features.
* **Interactive visual analytics** using Folium and Plotly Dash:
    - Folium maps + marker clusters: show launch sites;
    - Dashboard: show successes for all launch sites, success percentage per site, and payload per launch.
* **Predictive analysis using classification models:**
    - Split data between training and testing;
    - Train and test 4 models: LogReg (logistic regression), SVM (support vector machine), Tree (decision tree), KNN (K nearest neighbors);
    - Grid Search with a set of hyperparams; check model scores (R^2); build confusion matrix for each; —> select best model.

## Conclusions (Predictive Model)
* Out of 4 prediction models (LogReg, SVM, Tree, KNN), **SVM** had the best accuracy on training data, and among the best at scores on test data.
* The Tree model appeared the weakest.
* Test vs Training data accuracy are not the same.
* The dataset is too small (only 90 observations) to distinguish any further between these models

## See the Results 👇
[📁 Source Files](https://github.com/sinanthahir/Spacex_landing_prediction)  [📝 Report]()  [🌐 Dashboard]()