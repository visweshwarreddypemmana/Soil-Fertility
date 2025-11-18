
---

# 📘 Soil Fertility Prediction & Crop Recommendation System

*A complete Machine Learning workflow with feature engineering + ensemble modeling + crop advisory*

---

## 🌱 Overview

This project focuses on predicting **soil fertility levels** and recommending **best-suited crops** based on soil nutrient values.
I built this in **Python using Jupyter/Colab**, and the entire flow includes:

* Data exploration
* Advanced feature engineering
* Multiple ML models
* A weighted ensemble system
* A crop recommendation module
* Saved `.pkl` models for deployment

The goal was to develop a system that works well for real-world soil assessment.

---

## 📂 Project Structure

```
📁 Soil-Fertility-ML-Project
│── Soil Fertility Data.csv
│── Soil_Fertility.ipynb
│── soil_fertility_model.pkl
│── advanced_ensemble_model.pkl
│── advanced_soil_analysis_system.pkl
│── README.md
```

---

## 📊 Dataset Summary

The dataset contains **1288 soil samples** with **12 parameters**, including:

* N, P, K
* pH
* EC (Electrical Conductivity)
* Organic Carbon
* Sulphur
* Zinc, Iron, Copper, Manganese, Boron

### Fertility Labels

| Value | Meaning        |
| ----- | -------------- |
| **0** | Low Fertility  |
| **1** | Fertile        |
| **2** | High Fertility |

---

## 🧪 Exploratory Data Analysis

I explored the dataset using:

* Class distribution
* Histograms & boxplots
* Summary statistics
* Correlation heatmap
* Missing value detection

This helped in understanding nutrient variation and soil quality patterns.

---

## ⚙️ Baseline Preprocessing & Model

* Applied log transformations
* Performed 80/20 train-test split
* Trained a **RandomForestClassifier**
* Achieved **97.29% accuracy** on the first attempt

This served as the baseline before applying advanced techniques.

---

## 🔬 Advanced Feature Engineering

To increase the model’s ability to understand soil chemistry, I added **11 engineered features**, including:

### ✔ Nutrient Ratios

* N/P
* N/K
* P/K

### ✔ Soil Condition Indices

* Macronutrient Index
* Micronutrient Index

### ✔ Other Features

* pH suitability score
* Organic carbon efficiency
* EC category: Low / Optimal / High
* pH category: Acidic → Alkaline

After encoding and feature creation, the final dataset had **26 features**.

---

## 🤖 Ensemble Machine Learning Model

I built a weighted soft voting ensemble using:

| Model             | Notes               |
| ----------------- | ------------------- |
| Random Forest     | Balanced classes    |
| XGBoost           | Tuned parameters    |
| LightGBM          | Depth + leaf tuning |
| Voting Classifier | Soft voting         |

### Ensemble Weights

* Random Forest → **2**
* XGBoost → **1.5**
* LightGBM → **1.5**

### Outputs Generated

* Train-Test accuracy
* Individual model performance
* Feature importance ranking

The ensemble provided the most stable results.

---

## 🌾 Crop Recommendation System

I designed a class named `AdvancedCropRecommendation` that:

* Stores nutrient ranges for various crops
* Compares soil values with ideal nutrient ranges
* Recommends suitable crops
* Suggests improvements for deficient soils

Covered crops include:

Rice, Wheat, Maize, Millets, Pulses, Vegetables, Cotton, Soybean, Fruits, and more.

---

## 🌟 Final Results

| Model              | Train Accuracy | Test Accuracy |
| ------------------ | -------------- | ------------- |
| Random Forest      | 98–99%         | 96–97%        |
| XGBoost            | ~98%           | ~96%          |
| LightGBM           | 97–98%         | 95–96%        |
| **Ensemble Model** | **99%**        | **97–98%**    |

---

## 🚀 Why This Project?

I built this project to understand how machine learning can assist in **agricultural decision-making**, especially for soil analysis.
It combines:

* scientific understanding of soil
* practical feature engineering
* model tuning
* and a real-world recommendation system

---
