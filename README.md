# NetFlix-PredictionDescription-Length
# What Drives the Length of Description? Can We Predict It? what are the "rules" behind how Netflix tends to write descriptions ? 
# Objective: Predict whether a description will be long/short based on content type, genre, etc.
Questions to Answer:
 * Can we build a classification model to predict long vs. short descriptions?
 * Is there a correlation between type (movie/show) and description length?
# Skills Involved: 
Classification, feature engineering, NLP (basic). 

 note = “long descriptions = over 24 words” .

# confusion matrix LogisticRegression model :
![TV Shows vs Movies](téléchargement.png)

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
