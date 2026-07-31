# VortexTech AIML Week 3 - Regression & Clustering

## Dataset
Hospital Length of Stay Dataset (Microsoft), via Kaggle:
https://www.kaggle.com/datasets/aayushchou/hospital-length-of-stay-dataset-microsoft

## What I built
**Regression:** RandomForestRegressor predicting `lengthofstay` (days admitted) from 
patient health indicators. Chosen over Linear Regression since interactions between 
vitals (e.g. glucose + creatinine) affecting stay length are likely nonlinear.

**Clustering:** K-Means on hematocrit, bmi, and pulse (scaled). Elbow method used to 
pick k=3 — inertia drops sharply through k=3, then flattens.

## Files
- `vortextech_week3.ipynb` — full notebook, code + markdown explanations

## How to run
1. Clone repo: `git clone <repo-link>`
2. Open `.ipynb` in Google Colab
3. Run cells top to bottom
4. Upload the dataset CSV when prompted (Cell 1)

## Libraries used
pandas, scikit-learn, matplotlib, numpy

## Results
**Regression:**
- RMSE = 0.6301
- R² Score = 0.9276 (model explains ~93% of variance in length of stay)

**Clustering:**
- k = 3 chosen via elbow method
- Clusters separate mainly along BMI, with hematocrit as a secondary split — 
  likely reflecting different patient risk/comorbidity profiles
