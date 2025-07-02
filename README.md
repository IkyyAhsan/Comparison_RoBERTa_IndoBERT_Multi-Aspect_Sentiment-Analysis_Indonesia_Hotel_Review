# Aspect-Based Sentiment Analysis on Hotel Reviews (Facility Aspect Only)

This repository contains code and resources for performing **Aspect-Based Sentiment Analysis (ABSA)** on Indonesian hotel reviews, focusing **only on the "Facility" aspect**. The project compares two transformer-based models, **RoBERTa** and **IndoBERT**, using fine-tuning and hyperparameter optimization to classify sentiment as **positive** or **negative**.

## 📝 Project Overview

- **Goal**: To analyze user sentiment about hotel facilities from reviews written in Indonesian.
- **Aspect Focus**: `Facility`
- **Models Used**: `RoBERTa (cahya/roberta-base-indonesian-522M)` and `IndoBERT (indolem/indobert-base-uncased)`
- **Tuning Methods**: `Bayesian Optimization` and `Random Search`

## 📊 Dataset

- **Source**: Traveloka (scraped hotel reviews in Bandung, Indonesia)
- **Total Reviews (Facility Aspect)**: 2,000
  - Positive: 1,000
  - Negative: 1,000
- **Language**: Bahasa Indonesia

## ⚙️ Preprocessing Steps

1. Data Cleaning (removal of special characters, links, etc.)
2. Case Folding (conversion to lowercase)
3. Tokenization using respective model tokenizer (WordPiece or BPE)
4. Data Splitting (5-fold cross-validation)

## 🚀 Model Training

Two models are fine-tuned on the facility aspect dataset:
- **RoBERTa** with Bayesian Optimization
- **IndoBERT** with Random Search

### Evaluation Metrics:
- Accuracy
- Precision
- Recall
- F1-Score
- AUC

## ✅ Results (Facility Aspect)

| Model     | Accuracy | F1-Score | AUC    |
|-----------|----------|----------|--------|
| RoBERTa   | 85.35%   | 85.35%   | 88.98% |
| IndoBERT  | 95.65%   | 95.65%   | 96.90% |

✅ **IndoBERT outperforms RoBERTa** significantly in classifying sentiment for the facility aspect.
