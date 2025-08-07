# 🎧 Spotify Popularity Prediction

Predicting Spotify track popularity using audio features and machine learning models. Built as part of a university analytics course project at VCU, this repository includes data exploration, classification models, and business-driven insights for playlist strategy.

## 📌 Project Overview

This project investigates what makes a song popular on Spotify. Using a dataset of 5,000+ tracks and their audio features, we applied machine learning techniques to classify songs as “popular” or “not popular.” The final model achieved 82% test accuracy, selected based on its performance and business-aligned confusion matrix tradeoffs.

Beyond prediction, we also performed clustering and association rule mining to provide actionable playlist design recommendations based on traits like **speechiness** and **acousticness**.

## 📊 Dataset
- Records: 5,000+ songs
- Features:
  - Acousticness
  - Danceability
  - Energy
  - Instrumentalness
  - Liveness
  - Loudness
  - Speechiness
  - Tempo
  - Valence
  - Popularity (target variable)

## 🔍 Methods

### 1. **Data Cleaning & EDA**
- Handled missing/null values
- Explored feature correlations with target
- Visualized distributions and outliers

### 2. **Feature Engineering**
- Binned target into binary classes: Popular (≥65), Not Popular (<65)
- Normalized numerical features
- Removed highly collinear variables

### 3. **Modeling**
- Logistic Regression
- K-Nearest Neighbors
- Decision Tree Classifier

📈 **Model Evaluation:**
- Accuracy Score
- Confusion Matrix
- Precision / Recall
- Chosen model: **Logistic Regression (82% accuracy)**

### 4. **Business Optimization**
- Modeled cost of false positives vs. false negatives
- Selected model based on **revenue impact** of misclassification

### 5. **Clustering & Insights**
- KMeans clustering to explore user listening patterns
- Identified popular song traits: high speechiness + acousticness
- Recommended playlist design strategy based on findings

## 📌 Key Results

| Metric        | Value     |
|---------------|-----------|
| Final Model   | Logistic Regression |
| Test Accuracy | 82%       |
| Dataset Size  | 5,000+ songs |
| Key Predictors | Speechiness, Acousticness, Danceability |

## 💡 Business Recommendations

- Prioritize tracks with moderate acousticness and speechiness in curated playlists
- Target specific segments based on audio trait clusters
- Apply confusion matrix analysis for marketing strategy: minimize loss from false hits/misses

## 🛠️ Tools Used

- Python (pandas, numpy, matplotlib, sklearn)
- Jupyter Notebooks
- Seaborn & Plotly for visualization
- Scikit-learn for modeling
- Canva for final presentation visuals

## 🧠 Learnings

- Balancing model accuracy with business priorities is key in real-world analytics.
- Even basic models (like Logistic Regression) can outperform complex ones if tuned well and contextually selected.
- Visualization and storytelling are essential for stakeholder communication.


