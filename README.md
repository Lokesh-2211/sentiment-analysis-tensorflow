# Sentiment Analysis Using TensorFlow

This project is a Natural Language Processing (NLP) model that classifies financial text into three sentiment categories: **positive**, **negative**, or **neutral**. It was built using TensorFlow and Keras as part of a personal learning project to explore deep learning for financial applications.

---

## 📌 Overview

- 💬 **Task**: Sentiment classification of financial text
- 🧠 **Model**: Tuned neural network using Keras Tuner
- 📈 **Best Validation Accuracy**: **85.95%**
- 📂 **Dataset**: Custom dataset (`Sentences_75Agree_sample.txt`)
- 🧰 **Tools Used**: Python, TensorFlow, Keras, Pandas, Matplotlib, Keras Tuner

---

## 🧪 Example Use Case

```python
sample_texts = [
    "Markets are expected to rise after positive earnings reports.",
    "Economic slowdown may affect growth.",
    "The company held steady amid market uncertainty."
]

# Transform and predict
sample_features = vectorizer.transform(sample_texts)
predictions = final_model.predict(sample_features)
