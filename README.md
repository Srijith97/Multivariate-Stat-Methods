# Multivariate Statistical Analysis of Body Measurements & Fat

This project investigates how body measurements can be used to predict body fat percentage and Body Mass Index (BMI) using multivariate statistical techniques. Accurate body fat measurements are costly and inconvenient, so our goal was to identify simpler, accessible proxies using physical measurements.

📊 **Course**: STA 9705 (Spring 2025)  
👨‍🏫 **Instructor**: Professor Yu Yue  
🧑‍💻 **Contributors**:  
- Saisrijith Reddy Maramreddy  
- Peter Wong  
- Bryan Yeung  
- Zahidul Zahin  

---

## 📁 Dataset

We used the [Body Fat Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/body-fat-prediction-dataset) from Kaggle, which includes 252 male subjects and 15 physical attributes such as:

- Age, Height, Weight
- Abdomen, Chest, Hip, Thigh, Neck, Wrist, etc.
- Target: Body Fat %, Body Mass Index (BMI)

We cleaned the data by checking min/max values and removing rows with zero or missing entries.

---

## 🧠 Methods Used

### 1. **Multivariate Regression**
- Jointly modeled Body Fat % and BMI.
- Applied stepwise regression and Box-Cox transformations.
- Identified abdomen, forearm, wrist as strong predictors for body fat.
- Transformed models achieved R² ~0.73 (Body Fat), ~0.5 (BMI).

### 2. **MANOVA**
- Tested if body measurements differ by BMI and Body Fat % groups.
- Significant multivariate differences found across BMI and BFP levels.
- Specific contrasts (Normal vs. Overweight, Normal vs. High) also significant.

### 3. **Principal Component Analysis (PCA)**
- Applied PCA using both correlation and covariance matrices.
- Retained:
  - 4 PCs (correlation): ~83% variance explained.
  - 2 PCs (covariance): ~90% variance explained.
- Identified components related to fat distribution, age, and muscularity.

### 4. **Canonical Correlation Analysis (CCA)**
- Found two significant canonical correlations.
- Showed strong linear relationships between:
  - Body Fat/Density and Abdomen, Chest, Hip.
  - BMI and Height, Abdomen, Hip.

---

## 🔍 Key Findings

- Abdomen, hip, and chest are consistent strong predictors across models.
- Multivariate methods improve predictive performance and interpretability.
- Dimensionality reduction (PCA/CCA) helps simplify models without losing information.
- Even moderate changes in BMI/BFP show meaningful differences in body measurements.

---

## 🛠 Tools Used

- **SAS**: PROC GLM, PROC MANOVA, PROC PRINCOMP, PROC CANCORR
- **Statistical Techniques**: Multivariate Regression, MANOVA, PCA, Canonical Correlation

---

## 📎 References

- Rencher, *Methods of Multivariate Analysis*, Wiley
- Yue, Yu PhD., Lecture Notes & Chapter Summaries (MANOVA, PCA, CCA)
- SAS Institute Documentation
- [Kaggle Dataset](https://www.kaggle.com/datasets/fedesoriano/body-fat-prediction-dataset)

---

## 📂 Appendix

All SAS code and output figures are included in the appendix of the PDF report.
