# 📊 Text Feature Engineering - Data Processing Pipeline : Customer Reviews Analysis

## 🔍 Problem Statement

Businesses receive large volumes of customer reviews, making it difficult to manually extract insights.
This project builds a text processing pipeline to convert raw text into numerical features and perform sentiment classification.

---

## 📁 Dataset

* 100+ product reviews (Flipkart/Amazon-style dataset)
* Stored in CSV format with a `review_text` column

---

## ⚙️ Approach

### 1. Text Preprocessing

* Converted text to lowercase
* Tokenization
* Removed punctuation
* Removed stopwords
* Lemmatization

---

### 2. Feature Engineering

Implemented multiple techniques to convert text into numerical form:

* **One Hot Encoding** (manual implementation)
* **Bag of Words (BoW)** using CountVectorizer
* **TF-IDF** using TfidfVectorizer

---

### 3. Vocabulary Creation

* Built vocabulary from processed text
* Analyzed frequent words
* Evaluated vocabulary size

---

### 4. Sparse Matrix Analysis

* Generated feature matrices for BoW and TF-IDF
* Calculated sparsity (percentage of zero values)

👉 Observation:
Feature matrices are highly sparse, meaning most values are zero, which can lead to memory inefficiency in large-scale systems.

---

### 5. Model Building

* Logistic Regression
* Naive Bayes

Goal: Classify customer reviews into **positive** and **negative**

---

## 📊 Results & Observations

* TF-IDF performed better than Bag of Words in sentiment classification
* Bag of Words focuses on frequency, but ignores importance
* TF-IDF highlights important words by reducing weight of common terms

---

## ⚖️ Comparison of Techniques

| Method           | Advantage                | Limitation          |
| ---------------- | ------------------------ | ------------------- |
| One Hot Encoding | Simple representation    | High dimensional    |
| Bag of Words     | Captures word frequency  | No semantic meaning |
| TF-IDF           | Captures word importance | Ignores context     |

---

## 🧠 Key Insights

* Traditional NLP methods do not capture semantic meaning
* Words with similar meaning (e.g., "good" vs "excellent") are treated differently
* Sparse matrices can be inefficient for large datasets

---

## ❓ Real-World Considerations

* **Why BoW fails?**
  It does not capture semantic similarity between words

* **When to use BoW vs TF-IDF?**

  * BoW → simple tasks like spam detection
  * TF-IDF → tasks like sentiment analysis

* **Limitations of TF-IDF**

  * Does not understand context
  * Ignores word order

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* NLP techniques

---

## 📌 Conclusion

This project demonstrates how raw text data can be transformed into structured numerical features using NLP techniques.
It also highlights the strengths and limitations of traditional methods like Bag of Words and TF-IDF.

---

## 🚀 Future Improvements

* Use Word Embeddings (Word2Vec, GloVe)
* Apply Transformer models (BERT)
* Deploy as a real-time application

---
