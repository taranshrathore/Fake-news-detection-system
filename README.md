📰 Fake News Detection System
Spot fake news before it spreads — powered by NLP and Machine Learning.

   


🧠 About
Drop in any news article, and this app tells you in real time whether it's likely real or fake — no signup, no fluff, just a text box and an answer.

Under the hood, it's a full text-classification pipeline: raw article text gets cleaned, vectorized with TF-IDF, and classified by a Logistic Regression model trained on tens of thousands of labeled real and fake articles — hitting ~92% accuracy on held-out test data.

👉 Try it live


✨ Features
🔍 Instant classification — paste an article, get a REAL / FAKE verdict in under a second
📊 TF-IDF vectorization for lightweight, interpretable feature extraction
🤖 Logistic Regression classifier — fast inference, no GPU required
🧹 Clean preprocessing pipeline (stopword removal, tokenization, feature extraction)
🌐 One-click Streamlit web UI, deployed and publicly accessible
💾 Trained model + vectorizer persisted with joblib for instant reuse


🛠️ Tech Stack
Layer
Tools
Language
Python
ML / NLP
scikit-learn, TF-IDF, Logistic Regression
Data
pandas, NumPy
Model persistence
joblib
Web app
Streamlit
Training
Jupyter Notebook (app.ipynb)



📁 Project Structure
Fake-news-detection-system/

├── app.py              # Streamlit inference app

├── app.ipynb           # Model training & evaluation notebook

├── Fake.csv            # Fake news training data

├── True.csv            # Real news training data

├── requirements.txt    # Python dependencies

└── README.md


⚙️ Getting Started
1. Clone the repo
git clone https://github.com/taranshrathore/Fake-news-detection-system.git

cd Fake-news-detection-system
2. Install dependencies
pip install -r requirements.txt
3. Train the model (generates vectorizer.jb and lr_model.jb)
Run through app.ipynb to preprocess the data, train the TF-IDF + Logistic Regression pipeline, and export the model artifacts.
4. Launch the app
streamlit run app.py

Open the local URL Streamlit prints in your terminal, paste in a news article, and hit Check News.


📈 Model Performance
Algorithm: TF-IDF + Logistic Regression
Accuracy: ~92% on the test set
Evaluated using confusion matrix and classification report, with iteration on edge cases where model confidence was low


🔭 Future Improvements
Swap in transformer-based embeddings (BERT/DistilBERT) for higher accuracy
Add source/URL credibility scoring alongside text classification
Explainability layer (highlight the phrases driving the prediction)
Batch/CSV upload for classifying multiple articles at once


👤 Author
Taransh Rathore LinkedIn · GitHub


Built as part of exploring practical NLP + ML pipelines end-to-end — from raw text to a deployed, usable tool.

