# Steel Industry Load Type Prediction

## Overview

This project focuses on predicting the **Load\_Type** in a steel manufacturing environment using machine learning. It utilizes a dataset containing variables such as energy usage, reactive power, power factors, and CO2 emissions to classify operational loads into three categories:

* **Light\_Load (0)**
* **Maximum\_Load (1)**
* **Medium\_Load (2)**

## Objective

To build and evaluate various machine learning models that can predict the load type with high accuracy and generalizability, enabling better energy management and operational decisions in steel industries.

## Dataset

* Source:https://www.google.com/url?q=https%3A%2F%2Farchive.ics.uci.edu%2Fdataset%2F851%2Fsteel%2Bindustry%2Benergy%2Bconsumption
* Target Variable: `Load_Type`

### Features

* Usage\_kWh
* Lagging\_Reactive\_Power\_kvarh
* Leading\_Reactive\_Power\_kvarh
* CO2
* Lagging\_Power\_Factor
* Leading\_Power\_Factor
* NSM
* WeekStatus\_Weekend
* Day\_of\_week\_num

## Exploratory Data Analysis (EDA)

* Distribution plots and histograms to inspect skewness.
* Correlation matrix and heatmaps to identify relationships.
* Box plots to identify outliers.

## Preprocessing

* Handled skewness using log transformation.
* Applied scaling to features.
* Converted categorical values using OneHotEncoding.
* Splitting into training and test sets (80/20).

## Models Trained and Evaluated

1. Logistic Regression
2. Decision Tree Classifier
3. Support Vector Machine (SVM)
4. Multilayer Perceptron (MLP)
5. XGBoost Classifier

### Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1-Score

## Best Model: XGBoost

* Chosen based on performance across training and test data.

### Tuned Hyperparameters:

* `learning_rate`: 0.2
* `n_estimators`: 200
* `max_depth`: 5
* `subsample`: 0.8
* `colsample_bytree`: 1.0

### Final Evaluation:

* **Accuracy**: 90%
* **Precision**: 91%
* **Recall**: 90%
* **F1-Score**: 91%


## Conclusion

The XGBoost model generalizes well and is ideal for predicting load types in industrial settings. With a high F1-Score and accuracy, the model is deployment-ready.

## Future Work

* Deploy in real-time systems.
* Add anomaly detection for predictive maintenance.
* Continuously monitor model drift and retrain as needed.
