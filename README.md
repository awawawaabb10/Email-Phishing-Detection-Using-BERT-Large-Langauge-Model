# 📧 Email Phishing Detection Using BERT Large Language Model

## 📌 Description
This project implements **BERT (Bidirectional Encoder Representations from Transformers)** to accurately detect phishing emails. The model was evaluated under two scenarios:

1. **Scenario 1** – Using 7 individual phishing email datasets, compared against traditional machine learning models (**SVM, RF, ET, XGB, ADB**).  
2. **Scenario 2** – Using a large combined dataset containing **203,176 emails** to enhance the model's generalization capability.  

Experimental results show that **BERT** consistently outperforms traditional models in terms of **accuracy, precision, recall,** and **F1-score**.

---

## 📂 Dataset
The dataset consists of phishing and legitimate emails from 7 well-known public sources:
- Ling  
- Enron  
- SpamAssassin  
- TREC-05  
- TREC-06  
- TREC-07  
- CEAS-08  

📊 **Total combined dataset:** 203,176 emails  
📊 **Distribution:** 53% legitimate, 47% phishing

---

## ⚙️ Methodology
1. **Preprocessing**
   - Remove missing values & irrelevant characters
   - Convert all text to lowercase
   - Tokenize using **BERT WordPiece**
   - Maximum sequence length: 512 tokens

2. **Data Splitting**
   - Scenario 1: **Stratified 10-Fold Cross Validation**
   - Scenario 2: **80% training – 20% testing**

3. **Model**
   - **BERT Base** (12 encoder layers, hidden size 768)
   - Fine-tuned for binary classification (phishing / legitimate)

4. **Evaluation Metrics**
   - Accuracy
   - Precision
   - Recall
   - F1-Score
   - AUC-ROC

---

## 📊 Experimental Results

### Scenario 1 (Individual datasets)
- Highest accuracy: **99.64%** on the Ling dataset
- BERT outperforms nearly all traditional models
- On TREC-07, ET slightly outperformed BERT (99.85% vs 99.82%)

### Scenario 2 (Combined dataset)
- **Accuracy:** 99.35%  
- **Precision:** 99.45%  
- **Recall:** 99.04%  
- **F1-Score:** 99.24%  
- **AUC-ROC:** 99.97%  
- Only 78 **False Positives** and 148 **False Negatives** out of 40,102 test emails

---
