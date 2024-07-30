# Understanding YouTube Audience: Sentiment Analysis and Topic Modeling with NLP

This project performs sentiment analysis and topic modeling on YouTube comments from a specified video. The pipeline includes data collection, preprocessing, exploratory analysis, topic modeling, and sentiment analysis using various Natural Language Processing (NLP) techniques.

## Table of Contents

- [Introduction](#introduction)
- [Data Collection](#data-collection)
- [Data Preparation](#data-preparation)
- [Exploratory Analysis](#exploratory-analysis)
- [Topic Model Analysis](#topic-model-analysis)
- [Sentiment Analysis](#sentiment-analysis)
- [Requirements](#requirements)
- [License](#license)

## Introduction

This project aims to extract, preprocess, and analyze comments from a specified YouTube video. The analysis includes identifying the most common words, generating word clouds, performing n-gram analysis, extracting topics using LDA, and conducting sentiment analysis using both VADER and a rule-based approach based on parts of speech. Various NLP techniques are applied throughout the project to ensure robust text processing and analysis.

## Data Collection

YouTube comments are collected using the YouTube Data API. The `get_all_youtube_comments` function fetches all comments from a specified YouTube video and stores them in a CSV file.

## Data Preparation

Data preparation involves several NLP steps:
- Removing missing values
- Converting text to lowercase
- Expanding contractions
- Replacing URLs and HTML tags with labels
- Tokenization
- Lemmatization
- Removing stopwords
- Cleaning text by removing punctuation and non-alphabetic characters

## Exploratory Analysis

Exploratory analysis includes:
- Word frequency analysis
- Word cloud generation
- N-gram analysis for bigrams, trigrams, and four-grams

## Topic Model Analysis

Topic modeling is performed using Latent Dirichlet Allocation (LDA). The comments are tokenized and cleaned, and the LDA model is trained to extract topics. The dominant topic for each comment is identified, and the topics are evaluated using perplexity and coherence scores.

## Sentiment Analysis

Sentiment analysis is performed using two approaches:
1. **VADER Sentiment Analysis**: A lexicon-based approach that calculates sentiment scores for the original and cleaned comments.
2. **Rule-based Sentiment Analysis**: A custom approach based on parts of speech, where adjectives and adverbs are given higher weights in sentiment scoring.

## Requirements

The following packages are required to run the project:
- pandas
- google-api-python-client
- nltk
- contractions
- re
- wordcloud
- gensim
- matplotlib
- textblob


## License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/Adhish78/nlp-youtube-comments/blob/main/LICENSE) file for details.

