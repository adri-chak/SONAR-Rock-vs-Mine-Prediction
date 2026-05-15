# Sonar Rock vs Mine Prediction

This repository contains a machine learning project that uses **Logistic Regression** to classify underwater objects as either rocks or metal cylinders (mines) based on sonar signal frequencies.

## 🌊 The Story
Imagine a submarine navigating deep, treacherous waters. To avoid catastrophic collisions or hidden threats, it constantly emits sonar signals. These sound waves bounce off surrounding objects and return to the submarine, carrying unique frequency signatures. 

The critical challenge is distinguishing between a harmless **rock** and a dangerous **naval mine** purely from these echoes. This project automates that high-stakes decision-making process, transforming raw acoustics into actionable intelligence.

## 🎯 Use Case
* **Military & Defense:** Enhancing the autonomous detection capabilities of submarines and unmanned underwater vehicles (UUVs) to identify naval threats safely.
* **Marine Exploration:** Assisting deep-sea researchers in mapping the ocean floor by automatically filtering out geological formations from man-made debris.

## 📊 Dataset
The model is trained on the UCI Sonar Dataset, which includes:
* **208 total samples** of sonar return data.
* **60 numerical attributes** representing signal energy levels at different angles.
* **Binary target labels:** `M` for Mine (Metal Cylinder) and `R` for Rock.

## 🛠️ Implementation Procedure

1. **Data Collection:** Load the sonar data matrix into a Pandas DataFrame.
2. **Data Preprocessing:** 
    * Separate the 60 feature columns from the final classification label.
    * Split the dataset into **Training** and **Testing** subsets to evaluate performance on unseen data.
3. **Model Selection:** Deploy a Logistic Regression algorithm, which is ideal for binary classification and offers high interpretability.
4. **Training:** Fit the Logistic Regression model using the training subset.
5. **Evaluation:** Calculate the **Accuracy Score** on both training and test data to verify generalization.
6. **Prediction System:** Construct an inference loop that accepts a new array of 60 sonar values and outputs an instant `Rock` or `Mine` prediction.

