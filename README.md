# 🧠 Healthcare Review Sentiment Analysis

This project analyzes and classifies patient healthcare reviews into **positive**, **neutral**, or **negative** sentiments using Natural Language Processing (NLP) and machine learning.

---

## 📁 Project Structure

- `healthcare_sentiment_analysis.ipynb` – Main notebook/script for preprocessing, training, and evaluation.
- `sentiment_model.pkl` – Trained model file for deployment.
- `wordclouds/` – Visualizations showing frequent words per sentiment.
- `presentation.pptx` – Summary of findings.
- `report.pdf` – Detailed explanation of methods, results, and insights.

---

## 📊 Project Workflow

### 1. Data Preprocessing
- Removed null entries.
- Cleaned text using regex and tokenization.
- Removed stopwords using NLTK.

### 2. Text Analysis
- Visualized word frequencies and rating distributions.
- Generated word clouds for each sentiment.

### 3. Sentiment Mapping
- Mapped ratings to sentiments:
  - 1–2 → Negative  
  - 3 → Neutral  
  - 4–5 → Positive

### 4. Feature Extraction
- Used TF-IDF Vectorizer with unigrams and bigrams.

### 5. Model Training
- Built a pipeline with Naive Bayes + TF-IDF.
- Performed hyperparameter tuning using GridSearchCV.
- Evaluated with accuracy, ROC-AUC, and confusion matrix.

### 6. Handling Imbalance
- Applied **SMOTE** to handle class imbalance (neutral class underrepresented).
- Also tested a neural network after applying SMOTE.

---

## 🔧 Setup Instructions

### ✅ 1. Install Required Libraries

Make sure Python is installed. Then install the following packages:

```bash
pip install pandas numpy nltk scikit-learn matplotlib seaborn wordcloud joblib imbalanced-learn
```
### ✅ 2. Download NLTK Resources

The following lines are in the code. They will download what’s needed the first time:

```bash
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```
### ✅ 3. Run the Notebook

Open and run healthcare_sentiment_analysis.ipynb in Jupyter Notebook or any compatible IDE like VS Code.
