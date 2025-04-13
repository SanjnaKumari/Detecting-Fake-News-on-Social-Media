
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
