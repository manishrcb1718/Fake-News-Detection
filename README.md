# 📰 Fake News Detection

A simple machine learning project that predicts whether a news article is **Real** or **Fake** based on its **title**.

This project is beginner-friendly and uses classic, easy-to-understand tools: text cleaning, TF-IDF, and Logistic Regression.

---

## 🧠 What This Project Does

1. Loads a dataset of news articles (with titles and labels: Real/Fake)
2. Cleans and simplifies the titles (removing punctuation, stopwords, etc.)
3. Converts the text into numbers using **TF-IDF**
4. Trains a **Logistic Regression** model to classify news as Real or Fake
5. Tests the model's accuracy on unseen data
6. Lets you make a prediction on a sample article

---

## 📂 Files

| File | Description |
|------|-------------|
| `FND7.ipynb` | Jupyter Notebook containing all the code |
| `Dataset check.csv` | The dataset of news titles and labels (you need this file to run the notebook) |

> ⚠️ Make sure `Dataset check.csv` is in the **same folder** as the notebook before running it.

---

## 🛠️ Requirements

You'll need Python installed, along with these libraries:

```bash
pip install numpy pandas scikit-learn nltk
```

After installing, you also need to download NLTK's stopwords list (only once):

```python
import nltk
nltk.download('stopwords')
```

---

## ▶️ How to Run

1. Open a terminal or Anaconda Prompt.
2. Navigate to the project folder.
3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Open `FND7.ipynb`.
5. Run the cells **from top to bottom** (Shift + Enter for each cell).

---

## 🔍 How It Works (Step-by-Step)

### Step 1: Load the Data
The dataset is loaded using pandas, and missing values are filled with blank spaces.

### Step 2: Clean the Text (Stemming)
Each news title is cleaned by:
- Removing numbers/symbols (keeping only letters)
- Converting to lowercase
- Removing common "stopwords" (like "the", "is", "and")
- Reducing words to their root form (e.g., "running" → "run")

### Step 3: Convert Text to Numbers
Since machine learning models can't understand raw text, we use **TF-IDF (Term Frequency–Inverse Document Frequency)** to turn each title into a set of numbers representing how important each word is.

### Step 4: Split the Data
The dataset is split into:
- **80%** for training the model
- **20%** for testing how well it performs

### Step 5: Train the Model
A **Logistic Regression** model is trained on the training data to learn patterns that separate real news from fake news.

### Step 6: Check Accuracy
The model's accuracy is checked on both the training data and the test data to see how well it learned.

### Step 7: Make a Prediction
The notebook shows an example of predicting whether a single news title is Real or Fake.

---

## 📊 Example Output

```
train accuracy : 0.98
train accuracy : 0.95   (this is actually the test accuracy)
```

```
Fake News
```

---

## 💡 Notes for Beginners

- **TF-IDF** just means: "give more importance to unique/rare words, less importance to common words."
- **Stemming** just means: shortening words to their base form so "run", "running", and "runs" are all treated the same.
- **Logistic Regression** is a simple, popular algorithm used for yes/no (binary) classification problems — perfect for "Real vs Fake."

---

## 🚀 Possible Improvements

- Use the full article text instead of just the title
- Try other models (Random Forest, Naive Bayes, etc.)
- Build a simple web app (using Streamlit or Flask) so users can type in a headline and get a prediction
- Fix the small typo where the test accuracy print statement is labeled "train accuracy"

---

