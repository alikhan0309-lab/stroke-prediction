# Stroke Prediction

## Project Overview

This project explores whether patient health and demographic information can be used to predict the likelihood of stroke using machine learning.

The project includes data cleaning, exploratory data analysis, preprocessing, and a Logistic Regression model for stroke prediction.

## Research Question

Can patient health and demographic characteristics be used to predict the likelihood of stroke?

## Dataset

The project uses the **Stroke Prediction Dataset** from Kaggle.

The dataset includes variables such as:

* Gender
* Age
* Hypertension
* Heart disease
* Marital status
* Work type
* Residence type
* Average glucose level
* BMI
* Smoking status
* Stroke

The target variable is `stroke`.

* `0` = No stroke
* `1` = Stroke

## Data Cleaning

The following preprocessing steps were performed:

* Removed the `id` column because it is not useful for prediction.
* Removed the `Other` category from the gender variable.
* Filled missing BMI values using the median BMI.
* Checked the distribution of the target variable.

## Exploratory Data Analysis

Several visualizations were created to explore patterns in the data, including:

* Stroke vs. no-stroke counts
* Stroke rate by age group
* Stroke rate by hypertension and heart disease
* Glucose level and BMI by stroke status
* Correlation heatmap

These visualizations help identify patterns and relationships between patient characteristics and stroke occurrence.

## Machine Learning

The data was divided into training and testing sets using an 80/20 split with stratification to maintain the proportion of stroke and non-stroke cases.

### Preprocessing

Categorical variables were converted using **One-Hot Encoding**, while numerical variables were standardized using **StandardScaler**.

### Model

A **Logistic Regression** model was used as the initial classification model.

Because the stroke classes are highly imbalanced, `class_weight="balanced"` was used to give greater importance to the minority stroke class.

## Model Evaluation

Because the dataset is imbalanced, accurac
