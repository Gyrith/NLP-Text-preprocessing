# NLP Text Preprocessing: Hotel Reviews

A text preprocessing and sentiment analysis pipeline for 200 hotel reviews, built with NLTK and pandas.

## Pipeline

1. **Clean and tokenize:** lowercase, strip HTML and punctuation, expand contractions
2. **Normalize:** domain-specific stopwords (negations kept), POS-tagged lemmatization
3. **Analyze:** bigrams, trigrams and distinguishing words in positive vs. negative reviews
4. **Score:** VADER sentiment compared with star ratings
5. **Evaluate:** vocabulary and token reduction at each stage, with statistical tests

## Key results

- Vocabulary reduced by 20.2% 
- VADER matches rating-based sentiment 70% of the time; it struggles with neutral (3-star) reviews

## Run it

```
pip install pandas numpy nltk matplotlib seaborn scikit-learn scipy
jupyter notebook text_preprocessing_lab.ipynb
```

Keep `hotel_reviews.csv` in the same folder. NLTK data downloads on the first cell.