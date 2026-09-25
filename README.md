# Persian Sentiment Analysis 🇮🇷

A Natural Language Processing (NLP) project for sentiment analysis of Persian user reviews using Machine Learning and Deep Learning techniques.

## 📌 Project Overview

This project focuses on classifying Persian text into two sentiment classes:

- **HAPPY** 😊
- **SAD** 😞

The project uses the **SnappFood Persian Sentiment Analysis dataset** and compares a classical Deep Learning approach with a Persian Transformer-based model.

## 🎯 Objectives

- Preprocess and normalize Persian text
- Perform exploratory data analysis
- Build a vocabulary and prepare text sequences
- Train a **BiLSTM** sentiment classifier
- Fine-tune **ParsBERT** for Persian sentiment classification
- Compare model performance
- Perform error analysis
- Build a simple prediction interface using Gradio

## 📊 Dataset

The project uses the `ParsiAI/snappfood-sentiment-analysis` dataset.

Dataset splits:

| Split | Samples |
|---|---:|
| Train | 52,110 |
| Validation | 8,337 |
| Test | 9,033 |

The training data contains two balanced sentiment classes:

| Label | Samples |
|---|---:|
| HAPPY | 26,236 |
| SAD | 25,874 |

## 🧹 Text Preprocessing

Persian text preprocessing includes:

- HTML tag removal
- URL removal
- Persian text normalization
- Arabic-to-Persian character normalization
- Removing unwanted characters
- Removing extra spaces
- Tokenization

The preprocessing pipeline was implemented using **Hazm**.

## 🧠 Models

Two different approaches were implemented and evaluated:

### 1. BiLSTM

A Bidirectional Long Short-Term Memory neural network was trained using the processed Persian text sequences.

### 2. ParsBERT

A Persian BERT-based Transformer model was fine-tuned for binary sentiment classification.

## 📈 Results

The models were evaluated on the test set.

| Model | Accuracy | F1 Score |
|---|---:|---:|
| BiLSTM | 85.22% | 85.73% |
| ParsBERT | 87.18% | 87.97% |

## 🔍 Error Analysis

The test set contained **9,033 samples**.

The error analysis identified:

- **1,158 misclassified samples**
- Approximately **12.8%** of the test samples were misclassified
- **126** incorrect predictions were made with confidence above 90%

These examples were inspected to better understand the limitations of the models.

## 🖥️ Demo

A simple prediction interface was created using **Gradio**.

The interface allows users to enter Persian text and receive a sentiment prediction from the trained model.

## 🛠️ Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Hazm
- PyTorch
- Hugging Face Transformers
- Datasets
- Matplotlib
- Seaborn
- Gradio
- Google Colab

## 📁 Project Structure

```text
persian-sentiment-analysis/
│
├── Persian_Sentiment_Analysis.ipynb
├── README.md
├── requirements.txt
├── .gitignore
└── images/
