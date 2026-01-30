# Birth Dataset – Neural Network with Time-Series Feature Engineering

🎯 This project focuses on applying advanced preprocessing techniques on a time-based birth dataset before training a neural network model.

The dataset was transformed using the following key concepts:

✅ **Feature Engineering**  
✅ **Time-Series Feature Extraction**  
✅ **Rolling Window Features**  
✅ **Cyclic Encoding**

> “For time-based datasets, we extract features from date columns such as day, month, weekday, rolling window statistics, and cyclic encodings. These engineered features help the model learn seasonal and temporal patterns more effectively.”

This preprocessing approach allows the model to capture trends, seasonality, and short-term variations in birth data more accurately.

---

## About the Dataset
The birth dataset contains daily records of the number of births over a period of time.  
Since this is a time-based dataset, the date column plays a critical role in prediction and pattern discovery.

The target variable represents the **number of births**, making this a regression problem.

---

## Feature Engineering and Preprocessing

### 1. Date Feature Extraction
The original date column was split into multiple meaningful features:
- Day
- Month
- Year
- Weekday

This helps the model understand calendar-based patterns such as weekday behavior and seasonal effects.

---

### 2. Rolling Window Features
To capture short-term trends, rolling window features were created:
- Births in window size 5
- Births in window size 10
- Births in window size 15

These rolling statistics help the model learn recent trends rather than relying only on individual daily values.

---

### 3. Cyclic Encoding
Time-based features such as month and weekday are cyclic in nature:
- December → January
- Sunday → Monday

To preserve this cyclic relationship, sine and cosine transformations were applied:
- `sin`
- `cos`

This ensures that the model understands seasonality correctly.

---

### 4. Final Dataset Preparation
After feature engineering:
- Missing values were handled
- Features were scaled where necessary
- Final dataset was prepared for neural network training

---

## Neural Network Implementation
A neural network model was implemented to learn patterns from the engineered dataset:
- Input layer based on engineered features
- Hidden layers for pattern learning
- Output layer for birth count prediction

This helped in understanding how neural networks perform on structured time-series data after proper preprocessing.

---

## Objective
The main objective of this project is to demonstrate how time-series feature engineering significantly improves model learning compared to using raw date values.

---

## Results and Observations
- Feature engineering improved model learning behavior
- Rolling window features helped capture short-term trends
- Cyclic encoding improved seasonal understanding
- Neural network performance became more stable after preprocessing

---

## What I Learned
- Importance of feature engineering in time-based datasets
- Why raw date values are not meaningful for ML models
- How rolling window statistics improve predictions
- How cyclic encoding helps capture seasonality
- Applying neural networks to structured time-series data

---

## Repository Overview
This repository contains:
- Raw birth dataset
- Preprocessed and feature-engineered dataset
- Neural network implementation
- Supporting scripts and notebooks

---

## Author
Maulik Sindhva  
Computer Science Student
