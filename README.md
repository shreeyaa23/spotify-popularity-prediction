# Spotify Song Popularity Prediction

**Author:** Shreya Mishra   
**Institution:** Virginia Commonwealth University  

## Overview
This project predicts Spotify song popularity using machine learning models and analyzes musical traits that drive engagement. It compares accuracy-based and profit-based modeling to balance predictive performance with business impact.

## Objective
- Predict whether a song will be popular (popularity ≥ 65).  
- Compare Decision Tree, KNN, and Logistic Regression models.  
- Evaluate models on both accuracy and financial performance.  
- Identify key features influencing popularity.  
- Provide actionable recommendations to improve Spotify’s recommendation algorithms.

---

## Data Preparation
- **Dataset:** 5,000+ Spotify tracks with 15+ attributes.  
- **Missing Values:** Removed 499 incomplete rows for data integrity.  
- **Feature Selection:** Choose interpretable numerical and categorical attributes (danceability, energy, loudness, valence, etc.).  
- **Encoding:** Converted categorical fields (e.g., `explicit`) to numeric form.  
- **Target Variable:** Binary classification — 1 = Popular (≥ 65), 0 = Not Popular.

---

## Modeling and Evaluation

| Model | Accuracy | Key Findings |
|--------|-----------|--------------|
| **Decision Tree** | 0.54 | Speechiness, acousticness, and energy emerged as top predictors. |
| **K-Nearest Neighbor (K=5)** | 0.54 | Balanced generalization; useful for recommendation tasks. |
| **Logistic Regression** | 0.59 | Best overall accuracy; consistent results across folds. |

**Feature Importance (Logistic Regression):**
- Speechiness (0.145), Acousticness (0.107), Energy (0.099) were the most influential features.

---

## Profit-Based Analysis
Assumptions:  
- True Positive = +$1000  
- False Positive = –$700  
- False Negative = –$900  

| Model | Net Profit/Loss | Interpretation |
|--------|----------------|----------------|
| Decision Tree | –$24,300 | Best financial performance (low risk). |
| Logistic Regression | –$41,000 | Most accurate but higher loss. |
| KNN | –$55,900 | Moderate improvement from baseline. |

**Trade-Off:** Decision Tree maximized recall and minimized total loss, while Logistic Regression optimized accuracy.

---

## Advanced Analysis
- **Valence Effect:** Higher valence increased popularity odds by ~2.6%, indicating cheerful, energetic songs perform better.  
- **Clustering (Agglomerative, k=9):** Identified two dominant high-energy, high-loudness clusters (Silhouette ≈ 0.49).  
- **Association Rules (Apriori):** Genre crossovers such as *hiphop + pop → danceable + rnb* (Lift = 1.8) strongly correlate with success.

---

## Business Insights
1. Promote songs with higher **speechiness, acousticness, and energy**.  
2. Favor **high-valence, danceable tracks** for broader audience appeal.  
3. Apply **dual-model strategy:**  
   - Logistic Regression → precision playlisting (Discover Weekly).  
   - Decision Tree → profit-focused playlists (Top Hits, Viral 50).  
4. Use clustering for **mood-based playlist generation**.  
5. Target **genre crossovers (pop × hiphop × rnb)** to improve market reach.

---

## Tools and Technologies
- **Language:** Python  
- **Libraries:** pandas, numpy, scikit-learn, matplotlib, seaborn  
- **Techniques:** Grid Search CV, Clustering, Association Rule Mining  
- **Deliverables:** Jupyter Notebook, PDF report, and presentation slides  

---

## Results Summary
- Logistic Regression → Highest accuracy (59.6%)  
- Decision Tree → Highest profit retention (–$24.3K)  
- Clustering → Best segmentation (Silhouette ≈ 0.49)  
- Association Rules → High-lift patterns across top genres  

---

## Project Type
**Machine Learning · Classification · Business Analytics · Music Intelligence**
