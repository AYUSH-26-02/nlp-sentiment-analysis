# NLP Sentiment Analysis of Movie Reviews

A staged NLP project that plans and evaluates binary sentiment classification (positive vs. negative) on the Stanford Large Movie Review Dataset (IMDb/aclImdb).

## Project status
**Week 1 — Research and strategic planning.** This repository currently contains the research plan and project structure. Model training and performance results will be added only after experiments are run.

## Problem
Given an English-language movie review, predict whether its overall sentiment is positive or negative.

## Planned approach
1. Audit the public dataset and preserve its official train/test split.
2. Clean and normalize text without removing meaningful negation.
3. Explore class balance, review lengths, vocabulary and duplicates.
4. Convert text into TF-IDF features.
5. Compare Multinomial Naive Bayes, Logistic Regression and Linear SVC.
6. Select models using validation data and evaluate once on the untouched test set.
7. Report accuracy, precision, recall, macro F1, confusion matrix and error analysis.

## Dataset
Stanford Large Movie Review Dataset: https://ai.stanford.edu/~amaas/data/sentiment/

The labelled benchmark has 25,000 training and 25,000 test reviews (balanced positive/negative). Cite Maas et al. (2011) when using it. Do not upload the raw dataset to this repository unless its terms and repository size have been checked.

## Repository structure
```text
.
├── README.md
├── requirements.txt
├── .gitignore
├── docs/
│   └── Week1_NLP_Strategic_Planning_Report.docx
├── notebooks/
├── src/
└── reports/
    └── figures/
```

## Setup (for later implementation)
```bash
python -m venv .venv
# macOS/Linux
source .venv/bin/activate
# Windows
# .venv\Scripts\activate
pip install -r requirements.txt
```

## Research references
- Pang, Lee & Vaithyanathan (2002): https://aclanthology.org/W02-1011/
- Pang & Lee (2004): https://www.cs.cornell.edu/home/llee/papers/cutsent.home.html
- Maas et al. (2011): https://aclanthology.org/P11-1015/
- scikit-learn text feature extraction: https://scikit-learn.org/stable/modules/feature_extraction.html#text-feature-extraction

## Limitations
This is a binary movie-review benchmark, not a general-purpose sentiment system. Sarcasm, mixed opinions, domain shift and dataset bias remain important limitations.
