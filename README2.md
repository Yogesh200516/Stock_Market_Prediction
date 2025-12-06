# Task 2 — Logistic Regression Spam Classification

## 1. Introduction

This task involves building a machine learning model that classifies SMS messages as **Spam** or **Not Spam** using **Logistic Regression** only.  
No NLP or sentiment-analysis libraries were used.  
The model relies solely on Logistic Regression and a basic Bag-of-Words (BoW) text representation.

---

## 2. Dataset Information

- **File:** SPAM text message 20170820 - Data.csv  
- **Total messages:** 5572  
- **Columns used:**  
  - `label` — (spam / ham)  
  - `message` — SMS text  

Extra unnamed columns in the CSV were removed.

---

## 3. Objective Requirements

- Use **Logistic Regression**  
- Use at least **200 messages**  
- Use **150 training / 50 testing** or an **80:20 split**  
- **Do not** use NLP or sentiment-analysis libraries  
- Build a working classification model  

All requirements were successfully achieved.

---

## 4. Methodology

### 4.1 Data Loading
The dataset is loaded using `pandas`, and only the first two columns are retained.

### 4.2 Label Encoding
Text labels (spam/ham) are mapped to numeric values:
- ham → 0  
- spam → 1  

### 4.3 Text Vectorization (Allowed)
A simple **CountVectorizer (Bag-of-Words)** is used:
- Converts text to word-frequency vectors  
- No stemming, lemmatization, or NLP processing  
- Allowed because it is basic feature extraction  

### 4.4 Train–Test Split
An **80:20 split** was applied:
- Training samples: **4457**
- Testing samples: **1115**

This satisfies the minimum requirement of 150 training / 50 testing.

### 4.5 Model Training
The Logistic Regression classifier is trained using:


### 4.6 Model Evaluation
Evaluation metrics include:
- Accuracy  
- Precision  
- Recall  
- F1-score  
- Confusion matrix  

---

## 5. Results

### 5.1 Accuracy



### 5.2 Confusion Matrix

|                  | Predicted Ham | Predicted Spam |
|------------------|----------------|----------------|
| **Actual Ham**   | 966            | 0              |
| **Actual Spam**  | 22             | 127            |

### 5.3 Classification Report



---

## 6. Sample Predictions

| Message Example                                  | Model Prediction |
|--------------------------------------------------|------------------|
| Congratulations! You won a free voucher          | Not Spam         |
| Let's meet for lunch tomorrow                    | Not Spam         |
| URGENT! Your account has been suspended          | Not Spam         |

Some spam-like messages were misclassified due to BoW simplicity, but the task requirements were still fully met.

---

## 7. Conclusion

This task has been successfully completed.

- ✔ Logistic Regression used as required  
- ✔ Dataset processed and cleaned  
- ✔ 80:20 train–test split  
- ✔ No NLP or sentiment libraries  
- ✔ High accuracy (98%)  
- ✔ Full evaluation performed  

The project satisfies all specified objectives.

