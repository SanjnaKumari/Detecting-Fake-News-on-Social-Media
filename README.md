# 🧠 Detecting Fake News on Social Media: A Machine Learning Approach

Welcome! This project aims to tackle the widespread issue of **fake news** on social media using **machine learning** and **natural language processing (NLP)** techniques. We leverage the **LIAR dataset** from PolitiFact to train models that classify political news statements as **real** or **fake**.

> “Fake news spreads 6x faster than real news” — MIT study (2018)

---

## 📌 Project Overview

### 🔍 Objective
Develop robust ML models that classify news statements as either **true** or **false** to help mitigate the rapid spread of misinformation online.

### 🔬 Dataset: LIAR
- **Source:** PolitiFact, a Pulitzer Prize-winning fact-checking platform
- **Size:** 12,791 political statements
- **Original labels:** Six classes → **Mapped to binary**:
  - ✅ `True`: true, mostly-true, half-true
  - ❌ `False`: false, barely-true, pants-fire

---

## ⚙️ Methodology

### 1. 📊 Exploratory Data Analysis
- Distribution of real vs. fake statements
- Word clouds and frequency analysis
- Topic modeling using **LDA (Latent Dirichlet Allocation)**

### 2. 🧹 Data Preprocessing
- Lowercasing, punctuation removal, and stopword filtering
- Lemmatization and tokenization
- Label simplification (6-class to binary classification)

### 3. 📈 Feature Engineering
- BoW, TF-IDF, and GloVe embeddings (100-dim)
- Chi-Square selection of top 100 features (BoW & TF-IDF)
- Dropped metadata due to multicollinearity (high VIF)

---

## 🤖 Models Evaluated

| Model              | Best Feature Set | Test Recall |
|-------------------|------------------|-------------|
| Naive Bayes        | TF-IDF           | **92.36%**   |
| Support Vector Machine (SVM) | TF-IDF           | 84.23%     |
| Random Forest      | BoW              | 77.51%     |

> 🎯 **Recall** was prioritized to minimize false negatives (i.e., missing fake news)

---

## 📉 Evaluation Metrics

- **F1-Score**
- **Precision & Recall**
- **Confusion Matrix**
- **Cross-validation accuracy (5-fold)**

---

## 📊 Key Insights

- TF-IDF features consistently outperformed BoW and GloVe.
- Naive Bayes was best for maximizing recall.
- Metadata (e.g., speaker role/state) had high variance and redundancy → removed.
- Key discriminative words: *Obama, Clinton, healthcare, economy, tax, abortion*

---

## 🔐 Ethical Considerations

- This work is for **academic purposes only** and does not support censorship.
- Biases in the dataset are acknowledged and mitigated via cleaning.
- Designed to support **fact-checking tools**, not to silence opinion.

---

## 📚 Future Work

- Integrate deep learning models (BERT, LSTM)
- Real-time detection system using streaming data
- Incorporate multilingual datasets and metadata
- Explore stylometry and sentiment-based features

---

## 📜 Citation

If you use this project, please cite:

> Wang, W. Y. (2017). *"Liar, Liar Pants on Fire: A New Benchmark Dataset for Fake News Detection."* arXiv:1705.00648

---


🧠 Built with Python, Scikit-learn, NLTK, Gensim, and Matplotlib.
