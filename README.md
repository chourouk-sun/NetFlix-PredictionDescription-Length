# NetFlix-PredictionDescription-Length
# Objective: Predict whether a description will be long/short based on content type, genre, etc.
What Drives the Length of Description? Can We Predict It? what are the "rules" behind how Netflix tends to write descriptions ? 
# Questions to Answer:
  * Can we build a classification model to predict long vs. short descriptions?
  * Is there a correlation between type (movie/show) and description length?
 To answer this questions i built a machine learning model to predict Netflix description length using NLP & classification techniques. 
# Skills Involved: 
Classification, feature engineering, NLP (basic). 

note = “long descriptions = over 24 words” .
# Methodology:
i used the SMOTE methode to balance the training set.

# comparison table

| Metric              | Logistic Regression | Random Forest | XGBoost |
| ------------------- | ------------------- | ------------- | ------- |
| **Accuracy**        | 0.69                | 0.68          | 0.69    |
| **Precision (0)**   | 0.76                | 0.73          | 0.70    |
| **Recall (0)**      | 0.69                | 0.74          | 0.80    |
| **F1-Score (0)**    | 0.73                | 0.74          | 0.75    |
| **Precision (1)**   | 0.61                | 0.62          | 0.65    |
| **Recall (1)**      | 0.69                | 0.60          | 0.52    |
| **F1-Score (1)**    | 0.65                | 0.61          | 0.57    |
| **Macro Avg F1**    | 0.69                | 0.67          | 0.66    |
| **Weighted Avg F1** | 0.70                | 0.68          | 0.68    |



# confusion matrix LogisticRegression model :
!(confusionmatrix LogisticRegression.png)

 * Class 0 ( “Short”):
True Negatives (TN): 720 — correctly predicted as class 0
False Positives (FP): 318 — incorrectly predicted as class 1
 * Class 1 (“Long”):
False Negatives (FN): 222 — incorrectly predicted as class 0
True Positives (TP): 502 — correctly predicted as class 1

* **Accuracy** = (TP + TN) / Total = (720 + 502) / 1762 ≈ **0.69** : Good baseline   
* **Precision (Long)** = TP / (TP + FP) = 502 / (502 + 318) ≈ **0.61**  : Some false positives ✔
* **Recall (Long)** = TP / (TP + FN) = 502 / (502 + 222) ≈ **0.69** : Catches most long descriptions 
* **F1-score (Long)** ≈ **0.65** :  Balanced score ✔

  # Conclusion
- I built a classification model to predict whether a Netflix description is long or short.
- The best-performing model was Logistic Regression (Accuracy ≈ 69%).
- The model performs well, especially for very short descriptions.

