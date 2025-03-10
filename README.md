# Sentiment-Enhanced Product Recommendation System for E-Commerce: A Comparative Analysis of RoBERTa and VADER

## Overview

This project leverages advanced Natural Language Processing (NLP) techniques to analyze customer sentiment in e-commerce product reviews. By extracting emotional context from user-generated content, the system creates a sophisticated recommendation engine that goes beyond traditional rating systems. The implementation compares two leading sentiment analysis approaches—RoBERTa (an optimized BERT variant) and VADER—to determine which provides more accurate and nuanced understanding of customer opinions.

## Data

The analysis utilizes a comprehensive [Flipkart e-commerce dataset](https://www.kaggle.com/datasets/mansithummar67/flipkart-product-review-dataset/data) containing thousands of product reviews across diverse categories. Each record includes detailed product information (product name) alongside customer ratings, reviews and summaries, providing conducive context for sentiment extraction (opinion mining) and product evaluation.

## Methodology

The project implements a modular architecture with dedicated classes for (reference: flipkart_customer_product_review.ipynb):
- Data loading, validation and preprocessing
- Sentiment extraction using RoBERTa transformer models
- Lexicon-based sentiment analysis with VADER
- Comparative performance evaluation between approaches
- Visualization of relationships between price points, customer ratings, and sentiment scores
- Product ranking based on sentiment polarity metrics

The system extracts sentiment from both brief reviews and concise summaries (typically one or two sentences long), offering multi-dimensional analysis of customer opinions.

## Discussion

- Correlation patterns between product price and sentiment polarity
- Comparative performance analysis of transformer-based (RoBERTa) vs. lexicon-based (VADER) sentiment extraction
- Identification of sentiment-price-rating relationships that can inform pricing strategies
- Optimized recommendation algorithms that prioritize products with consistently positive sentiment patterns

## Applications
This sentiment-enhanced recommendation system can help e-commerce platforms improve customer satisfaction by recommending products that genuinely resonate with users, potentially increasing conversion rates and reducing return frequencies.

## Technologies
Python, PyTorch, Transformers (BERT, RoBERTa), NLTK, Pandas, Matplotlib, Seaborn, HuggingFace

