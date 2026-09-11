# 🎬 Movie Review Sentiment Analysis using NLP & Machine Learning

## 📌 Project Overview

This project performs **sentiment analysis on movie reviews** using Natural Language Processing (NLP) and Machine Learning techniques.

The system processes movie reviews, cleans and transforms the text into numerical features using **TF-IDF**, and uses a **Logistic Regression classifier** to predict whether a review is **Positive** or **Negative**.

A **Deep Learning ANN model using TensorFlow** was also explored theoretically, but it was not executed due to Python/TensorFlow compatibility limitations in the development environment.

---

## 🎯 Objectives

* Analyze movie reviews using NLP techniques.
* Clean and preprocess textual data.
* Convert text into numerical features using TF-IDF.
* Encode sentiment labels into numerical values.
* Train a Machine Learning classification model.
* Evaluate the model using accuracy, confusion matrix, and classification report.
* Understand how Artificial Neural Networks can be applied to sentiment analysis.

---

## 📂 Dataset

The project uses the **IMDB Movie Review Dataset**.

The dataset contains movie reviews labeled as:

* `positive`
* `negative`

The main columns used are:

| Column      | Description                    |
| ----------- | ------------------------------ |
| `review`    | Movie review text              |
| `sentiment` | Positive or negative sentiment |

The original dataset is **not included in this repository** because the CSV file exceeds GitHub's browser upload size limit.

### Dataset Setup

Download the IMDB Dataset and place it in the project directory before running the notebook:

```text
Movie-Review-Sentiment-Analysis/
│
├── IMDB Dataset.csv
└── Movie_Review_Sentiment_Analysis.ipynb
```

---

## 🔄 Project Workflow

```text
IMDB Movie Reviews
        ↓
Text Cleaning
        ↓
Lowercase Conversion
        ↓
Remove Punctuation & Special Characters
        ↓
Tokenization
        ↓
Stopword Removal
        ↓
Lemmatization
        ↓
Label Encoding
        ↓
TF-IDF Vectorization
        ↓
Train-Test Split
        ↓
Logistic Regression
        ↓
Prediction
        ↓
Model Evaluation
```

---

## 🧹 NLP Preprocessing

The reviews are processed using several NLP techniques.

### 1. Lowercase Conversion

All reviews are converted to lowercase to maintain consistency.

### 2. Text Cleaning

Punctuation and special characters are removed using regular expressions.

### 3. Tokenization

Reviews are split into individual words using **NLTK**.

### 4. Stopword Removal

Common English words that provide little sentiment information are removed.

### 5. Lemmatization

Words are converted to their base form using **WordNetLemmatizer**.

---

## 🔢 Label Encoding

The sentiment labels are converted into numerical values:

```text
Negative → 0
Positive → 1
```

This allows the Machine Learning model to process the target variable.

---

## 📊 TF-IDF Vectorization

Machine Learning models cannot directly understand raw text.

**TF-IDF (Term Frequency–Inverse Document Frequency)** is used to convert the processed reviews into numerical feature vectors.

The project uses a maximum of **5,000 features**.

```python
TfidfVectorizer(max_features=5000)
```

---

## 🤖 Machine Learning Model

### Logistic Regression

Logistic Regression is used as the primary classification model.

```python
LogisticRegression(max_iter=1000)
```

The model is trained using an **80:20 train-test split**.

```text
Training Data → 80%
Testing Data  → 20%
```

A fixed `random_state=42` is used to make the experiment reproducible.

---

## 📈 Model Evaluation

The model is evaluated using:

### Accuracy

Measures the overall percentage of correctly classified reviews.

### Confusion Matrix

Shows:

* Correctly predicted positive reviews
* Correctly predicted negative reviews
* Incorrect positive predictions
* Incorrect negative predictions

### Classification Report

The classification report provides:

* Precision
* Recall
* F1-score
* Support

---

## 🧠 Deep Learning Exploration

An **Artificial Neural Network (ANN)** using TensorFlow was planned as a comparison between traditional Machine Learning and Deep Learning.

However, the ANN implementation could not be executed because of **Python/TensorFlow compatibility limitations** in the development environment.

Therefore:

* Logistic Regression → **Implemented and evaluated**
* ANN → **Explored theoretically but not executed**

This project therefore focuses on the successfully implemented **NLP + Logistic Regression pipeline**.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **NLTK**
* **Scikit-learn**
* **TF-IDF**
* **Logistic Regression**
* **TensorFlow** — explored for ANN

---

## 📁 Project Structure

```text
Movie-Review-Sentiment-Analysis/
│
├── notebooks/
│   └── Movie_Review_Sentiment_Analysis.ipynb
│
├── screenshots/
│   ├── sentiment_distribution.png
│   ├── model_results.png
│   └── sentiment_prediction.png
│
└── README.md
```

> **Note:** The IMDB CSV dataset is not stored in this repository because of its large file size.

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/johnvalentina1413-stack/Movie-Review-Sentiment-Analysis.git
```

### 2. Install the required libraries

```bash
pip install pandas numpy matplotlib nltk scikit-learn
```

If TensorFlow experimentation is required:

```bash
pip install tensorflow
```

### 3. Download the IMDB dataset

Place:

```text
IMDB Dataset.csv
```

in the required project directory.

### 4. Open the notebook

Open:

```text
Movie_Review_Sentiment_Analysis.ipynb
```

and run the cells sequentially.

---

## ⚠️ Limitations

* The model is trained on a fixed IMDB movie-review dataset.
* It is not connected to live movie-review platforms.
* Only positive and negative sentiment classes are considered.
* The ANN section was not executed because of environment compatibility issues.
* Model performance may vary depending on preprocessing and train-test split.
* TF-IDF is limited to the selected 5,000 features.

---

## 🔮 Future Improvements

* Implement and evaluate the ANN using a compatible TensorFlow environment.
* Compare Logistic Regression with Naive Bayes, SVM, and other classifiers.
* Experiment with Word2Vec or other word embeddings.
* Use LSTM/GRU models for deep learning-based sentiment analysis.
* Implement Transformer-based models such as BERT.
* Create a Streamlit web interface for real-time review sentiment prediction.
* Add support for more sentiment categories such as neutral or mixed.

---

## 📚 Learning Outcomes

Through this project, the following concepts were practiced:

* Exploratory Data Analysis
* Text preprocessing
* Tokenization
* Stopword removal
* Lemmatization
* Label Encoding
* TF-IDF feature extraction
* Train-test splitting
* Logistic Regression
* Classification evaluation
* Confusion Matrix
* NLP workflow design
* Introduction to Deep Learning concepts

---

## 👩‍💻 Author

**Valentina John**

BSc Information Technology

Interested in **Cybersecurity, Machine Learning, NLP, Data Analytics, and Software Development**.
