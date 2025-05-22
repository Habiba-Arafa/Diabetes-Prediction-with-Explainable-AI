
#  Diabetes Diagnosis using Machine Learning, Deep Learning, and Explainable AI


## Abstract

This project explores the predictive modeling of diabetes using both traditional Machine Learning (ML) and Deep Learning (DL) approaches, combined with Explainable AI (XAI) techniques. The PIMA Indian Diabetes Dataset was used to evaluate multiple models, perform feature selection, and apply interpretability methods including SHAP, LIME, PDP, ICE, LOFO, PFI, Global Surrogate Tree models. The study aims to offer high-accuracy predictions while maintaining transparency crucial for clinical decision-making.

---

##  Problem Statement

Diabetes is a global health challenge, and its early detection can significantly improve patient outcomes. However, the adoption of AI-based diagnostic tools in clinical settings is limited by their lack of transparency. This study focuses on:
- Comparing ML and DL models for diabetes diagnosis.
- Enhancing interpretability using XAI techniques.
- Evaluating clinical applicability of interpretable models.

---

##  Dataset

- **Source:** PIMA Indian Diabetes Dataset (Kaggle)
- **Records:** 768
- **Features:** 8 input features + 1 binary outcome (`Outcome`)
- **Key Features:** Glucose, BMI, Age, Insulin, Pregnancies, BloodPressure, DiabetesPedigreeFunction

---

##  Methodology

### 1. Exploratory Data Analysis (EDA)
- Visualization: Histograms, Heatmaps
- Insights: Glucose is the strongest predictor; class imbalance present

### 2. Preprocessing
- Handling imbalance using undersampling and ADASYN
- Outlier detection
- Scaling and normalization
- PCA and t-SNE for visualization

### 3. Feature Selection
- Techniques: Chi-square, ANOVA, RFE, Information Gain, Relief, Forward/Backward Selection
- Final Top 7 Features: Glucose, BMI, Age, Insulin, Pregnancies, BloodPressure, DiabetesPedigreeFunction

### 4. Model Training
- **ML Models:** SVM, Random Forest, XGBoost, KNN, Voting Classifier
- **DL Models:** ANN, ConvLSTM, BPNN
- **Tuning:** GridSearchCV, 5-fold Cross-Validation

---

## Evaluation Metrics

- Accuracy
- Precision
- Recall (Sensitivity)
- Specificity
- F1-Score
- ROC-AUC
- Learning and validation curves

---

##  Explainable AI (XAI)

### Tools Used:
- **SHAP:** Global and local feature importance
- **LIME:** Instance-level prediction explanations
- **PDP & ICE:** Feature effect visualization
- **LOFO:** Performance drop after feature removal
- **PFI:** Impact of feature value shuffling
- **Surrogate Trees:** Model approximation via decision trees

### XAI Evaluation Metrics:
- Fidelity
- Faithfulness
- Stability
- Consistency

---

## Results

| Model            | Accuracy |
|------------------|----------|
| Random Forest    | 89%      |
| BPNN             | 89%      |
| XGBoost          | 85%      |
| Voting Classifier| 85%+     |
| SVM              | 83%+     |

- **Best Explainer:** SHAP for both global and local insights
- **Key Features:** Glucose, BMI, Age
- **Challenge:** DL models underperformed due to dataset size

---

##  Key Findings

- Feature selection significantly boosts accuracy and interpretability.
- Ensemble models like XGBoost achieve a balance between accuracy and explainability.
- SHAP and LIME are effective for medical decision support.
- Interpretability tools offer both global insights and patient-level justifications.

---

##  Limitations

- Small dataset size restricts DL performance
- SHAP computational cost is high
---

##  Conclusion

The integration of ML/DL models with robust XAI techniques provides a reliable framework for diabetes diagnosis. While models like Random Forest and BPNN achieve high accuracy, explainability tools like SHAP and LIME ensure transparency and trust in AI-driven clinical decision support systems.

---

##  References

Full references are provided in the paper and include works on XAI, ensemble models, SHAP, LIME, and applications of ML in healthcare.
