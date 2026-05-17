# 📝 Part 3: NLP and Sequence Modeling

## 📌 Overview

This project focuses on building an NLP pipeline to classify customer support messages based on sentiment. It compares traditional text vectorization methods with sequence-based deep learning approaches.

---

## 🎯 Problem Statement

The task is to classify customer messages into one of three sentiment categories:

* Positive
* Neutral
* Negative

This is a **multi-class text classification problem**.

---

## 📂 Dataset

### 📂 Setup Instructions

The dataset is not included in this repository as per submission guidelines.

Please download the dataset from the following link:

👉 https://drive.google.com/drive/folders/1akV6po4Nrgkc3yQrJkzA6cJlV-wBvUYs?usp=sharing

---

### 📁 Setup Steps:

1. Download the dataset
2. Extract the files
3. Place the file `customer_support_text_classification.csv` inside the `dataset/` folder

---

### 📁 Final Structure

  part-3-nlp-sequence-modeling/
  
    ├──_ notebook.ipynb
    ├── README.md
    ├── dataset/
    │   └── customer_support_text_classification.csv

---

### 📊 Dataset Description

The dataset contains customer support messages used for sentiment classification.

* Input column: `customer_message`
* Target column: `sentiment_label`

  * positive
  * neutral
  * negative

Additional fields:

* `channel`
* `word_count`
* `urgent_flag`

---

### ⚠️ Note

If the dataset file is not present in the `dataset/` folder, the notebook will not run and will prompt the user to download it.

## 🔍 Dataset Understanding

* Total records: 1500
* Target classes: positive, neutral, negative

### 📊 Observations:

* Sample messages include customer queries, complaints, and feedback
* Average text length: (add your value) words
* Dataset is (balanced / slightly imbalanced — based on your output)

---

## 🧹 Text Preprocessing

The following preprocessing steps were applied:

* Lowercasing text
* Removing special characters
* Tokenization (splitting into words)
* Stopword removal
* Conversion to sequences using tokenizer
* Padding sequences to fixed length (50)

---

## 🔢 Text Vectorization

### 🔹 TF-IDF Representation

* Converts text into numerical vectors
* Assigns importance to words based on frequency and uniqueness

### 🔹 Why Vectorization?

Machine learning models cannot process raw text.
Text must be converted into numerical form for model input.

---

## 🤖 Baseline Model

A baseline model was built using:

* **Logistic Regression + TF-IDF**

### 📊 Performance:

* Accuracy: (add your value)

### 🔍 Evaluation:

* Classification report (precision, recall, F1-score)
* Confusion matrix

---

## 🔁 Sequence Model (LSTM)

A sequence-based deep learning model was built using LSTM.

### 🧱 Architecture:

* Input sequences (padded)
* Embedding layer (word representation)
* LSTM layer (captures sequence dependencies)
* Dense layer
* Output layer (softmax for 3 classes)

### ⚙️ Configuration:

* Loss: Sparse Categorical Crossentropy
* Optimizer: Adam
* Metric: Accuracy

---

## ⚖️ Model Comparison

| Approach                     | Strength                        |
| ---------------------------- | ------------------------------- |
| TF-IDF + Logistic Regression | Fast, simple, strong baseline   |
| LSTM                         | Captures word order and context |

---

## 🧠 Attention and Transformers

### 🔹 RNN Limitation

RNNs struggle with long-term dependencies due to vanishing gradients.

### 🔹 LSTM Advantage

LSTMs use gating mechanisms to retain important information.

### 🔹 Attention Mechanism

Allows models to focus on important words in a sequence.

### 🔹 Transformers

Modern NLP models use attention for better context understanding and faster computation.

---

## 🚀 Conclusion

* Traditional methods like TF-IDF provide strong baseline performance
* Sequence models like LSTM improve contextual understanding
* Modern NLP relies on attention and transformer architectures for advanced tasks

---

## 🛠️ Technologies Used

* Python
* Pandas, NumPy
* Scikit-learn
* NLTK
* TensorFlow / Keras
* Matplotlib, Seaborn

---

## 📎 Note

Dataset is referenced from the provided project folder and is not included in this repository as per submission guidelines.
