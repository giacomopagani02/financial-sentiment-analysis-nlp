# Financial Sentiment Analysis with NLP and Deep Learning

## Project Overview
This project develops a financial sentiment analysis system using both classical machine learning and deep learning techniques.

The goal is to classify financial news text into **positive, neutral, or negative sentiment**, supporting decision-making in financial contexts.

## Dataset
- Final dataset: ~35,000 observations after cleaning
- Sources:
  - Financial PhraseBank
  - Large-scale financial news dataset
- Balanced classes (~8000 per class)

## Methodology

### 🔹 Text Representations
- Bag of Words (BoW)
- TF-IDF
- Word2Vec embeddings

### 🔹 Models
- Logistic Regression
- Support Vector Machine (SVM)
- Bidirectional LSTM (BiLSTM)

### 🔹 Pipeline
- Text cleaning & normalization
- Tokenization & lemmatization
- Feature extraction / embeddings
- Train / validation / test split

## Deep Learning Approach
- BiLSTM with Word2Vec initialization
- Dropout + recurrent dropout
- Early stopping & learning rate scheduling

## Results

| Model          | F1 Score |
|----------------|--------|
| **BiLSTM**     | **0.7255** |
| SVM + BoW      | 0.7232 |
| LR + BoW       | 0.7183 |
| SVM + TF-IDF   | 0.7037 |
| LR + TF-IDF    | 0.7022 |

Best model: **BiLSTM with Word2Vec embeddings**

## Key Insights
- BoW outperforms TF-IDF in financial text
- Classical models are highly competitive
- Deep learning improves performance only with good embeddings
- Financial language is highly ambiguous and context-dependent

## Explainability (XAI)
- SHAP used to interpret BiLSTM predictions
- Identifies key words driving sentiment decisions
- Highlights ambiguity of terms like "down"

## Ethical Considerations
- Model bias across sentiment classes
- Importance of explainability in finance
- Human-in-the-loop decision making

## Tools & Technologies
- Python
- Scikit-learn
- TensorFlow / Keras
- Word2Vec
- SHAP
- Google Colab

## Full Report
See `report.pdf` for full methodology and analysis.

## Authors
- Giacomo Pagani
- Gabriele Ferraresi
- Alessia Lecchi
