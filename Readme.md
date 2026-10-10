# NLP Text Preprocessing: Hotel Reviews

A text preprocessing and sentiment analysis pipeline for 200 hotel reviews, built with NLTK and pandas. The goal is to turn messy review text into clean, structured data that shows which issues appear in negative reviews and which strengths could be promoted in marketing.

## Pipeline
**Clean and tokenize:** split reviews into sentences and word tokens, lowercase, remove punctuation and special characters, expand contractions (n't becomes not)
**Normalize:** remove stopwords using a domain-specific list (negations kept), then apply POS-tagged lemmatization
**Analyze:** bigrams, trigrams and distinguishing words in positive (4-5 stars) vs. negative (1-2 stars) reviews
**Score:** VADER sentiment compared with star-rating sentiment (positive 4-5, neutral 3, negative 1-2)
**Evaluate:** vocabulary size and token counts at each stage, with percentage reductions
## Key results
Unique tokens reduced by 20.2% from raw text to the lemmatized form (RAW_COUNT to FINAL_COUNT unique tokens)
VADER agrees with rating-based sentiment 70% of the time on lemmatized text; it struggles most with neutral (3-star) reviews, which often mix praise and complaints in one review
**INSIGHT:** top complaints in negative reviews and top strengths in positive reviews (fill in from your n-gram output)
The required NLTK data downloads when you run the first cell.

## Files
text_preprocessing_lab.ipynb: the full analysis, with outputs
hotel_reviews.csv: 200 hotel reviews (review text, rating, date)