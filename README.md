# Monster Hunter Wilds: Steam Review NLP Analysis

## Objective
MHWilds launched to a highly polarized reception on Steam. The goal of this project was to bypass the noise of standard review scores and use Natural Language Processing (NLP) to extract why the player base was frustrated, isolating the specific features and bugs driving negative sentiment.

## Tech Stack
* Data Ingestion: `requests` (Steamworks API)
* Data Processing: `pandas`, `re` (Regular Expressions)
* NLP & Sentiment Analysis: `TextBlob`, `NLTK` (Stopwords & N-grams)
* Data Visualization: `matplotlib`, `seaborn`

## Pipeline
1. API Scraping: Built a custom pagination scraper to extract raw JSON reviews directly from Steam API.
2. Text Preprocessing: Vectorized a Pandas pipeline to sanitize text (lowercasing, regex punctuation removal, squishing whitespaces).
3. Sentiment Scoring: Utilized TextBlob's lexicon-based model to assign polarity scores (-1.0 to 1.0) to every review.
4. Feature Extraction: Filtered for highly negative reviews and utilized NLTK Bigrams (combined with a custom gaming domain-lexicon) to extract the most frequent two-word contextual complaints.

## Key Findings
Average sentiment score hovered barely above neutral at 0.105. Most common complaints were related to performance issues.