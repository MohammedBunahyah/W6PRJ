# 🧠 Automated Amazon Review Insights using NLP & Generative AI

A full-stack Natural Language Processing (NLP) project to classify, cluster, and summarize product reviews from Amazon using transformer models and deploy the solution as a web app.

---

## 🚀 Project Overview

**Goal:**  
To automate the analysis of thousands of product reviews using NLP and provide clear product recommendations in the form of sentiment classification, product grouping, and review summarization.

---

## 📌 Features

- ✅ **Sentiment Classification** using BERT
- ✅ **Product Clustering** with TF-IDF and KMeans
- ✅ **Review Summarization** using BART (Generative AI)
- ✅ **Interactive Web App** built with Gradio
- ✅ **Model Evaluation** with metrics, misclassifications, and confidence scores

---

## 📁 Project Structure

. ├── data/ # Amazon review datasets ├── notebooks/ # Jupyter notebooks (EDA, modeling, summarization) ├── my_finetuned_bert_model/ # Trained BERT model saved locally ├── app/ # Gradio app code ├── README.md └── requirements.txt

yaml
Copy
Edit

---

## 🔍 Model Highlights

### Sentiment Classification
- Pretrained model: `bert-base-uncased`
- Accuracy: ~83%
- F1-Scores:  
  - Positive: 0.89  
  - Neutral: 0.71  
  - Negative: 0.86  

> Originally tried DistilBERT (~71% accuracy). Switched to BERT for better performance.

---

### Product Clustering
- Method: `TF-IDF + KMeans (k=5)`
- Manually inspected clusters:
  - Ebook readers
  - Batteries
  - Accessories
  - Household / pet items
  - Miscellaneous

---

### Review Summarization
- Model: `facebook/bart-large-cnn`
- Output: Article-style summaries per product cluster
  - Top 3 products with differences
  - Most common complaints
  - Worst product

---

## 🧪 How to Run

### 1. Clone the Repo
```bash
git clone https://github.com/yourusername/nlp-amazon-reviews.git
cd nlp-amazon-reviews
2. Install Requirements
bash
Copy
Edit
pip install -r requirements.txt
3. Run Model Training
Inside the appropriate notebook (or script), run:

sentiment_classifier.ipynb to fine-tune BERT

clustering.ipynb to group products

summarization.ipynb for summaries

4. Launch Web App
bash
Copy
Edit
cd app
python gradio_app.py
🌐 Gradio Demo
🔗 Live App (if hosted)
Or launch locally using gradio_app.py.

🧠 Key Learnings
Model choice has a big impact — BERT outperformed DistilBERT significantly.

Neutral sentiment is the hardest to classify due to ambiguity.

TF-IDF + KMeans is effective for unsupervised product grouping.

Gradio makes deploying NLP apps fast and easy.

📚 Dataset
Datafiniti Amazon Product Reviews (via Kaggle)

Cleaned and balanced to 500 samples per sentiment class

📦 Dependencies
transformers

scikit-learn

datasets

gradio

nltk, pandas, matplotlib, seaborn

📜 License
MIT License © 2025 Mohammed Bunahyah

