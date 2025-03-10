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

  <div style="display: flex; flex-direction: column; gap: 30px; margin-bottom: 30px;">
  <div>
    <figure style="margin: 0; padding: 0; display: flex; flex-direction: column; align-items: center;">
      <a href="https://github.com/newking9088/product_recommendation_nlp_roberta_vader/blob/main/roberta_sentiment_analysis.png" target="_blank">
        <img src="https://github.com/newking9088/product_recommendation_nlp_roberta_vader/blob/main/roberta_sentiment_analysis.png" 
             alt="RoBERTa Sentiment Analysis Results" 
             style="width: 100%; max-width: 800px; height: auto;">
      </a>
    </figure>
  </div>

  <br>
  <div>
    <figure style="margin: 0; padding: 0; display: flex; flex-direction: column; align-items: center;">
      <a href="https://github.com/newking9088/product_recommendation_nlp_roberta_vader/blob/main/vader_sentiment_analysis.png" target="_blank">
        <img src="https://github.com/newking9088/product_recommendation_nlp_roberta_vader/blob/main/vader_sentiment_analysis.png" 
             alt="VADER Sentiment Analysis Results" 
             style="width: 100%; max-width: 800px; height: auto;">
      </a>
  </div>
</div>

The comparison shows distinct patterns between both sentiment analysis models: RoBERTa displays more cautious sentiment assignment with higher neutral classifications (43.5% for reviews vs. VADER's 39.4%), while VADER tends to assign more positive sentiment (53.4% for reviews and 75.8% for summaries compared to RoBERTa's 46.9% and 69.4%). Though RoBERTa likely offers superior contextual understanding and nuance detection, it required approximately 1000x longer processing time than VADER's efficient lexicon-based approach. For a definitive accuracy assessment, human-annotated ground truth labels would be necessary to evaluate which model better captures authentic sentiment, particularly in cases where contextual understanding significantly impacts interpretation.

The top 10 recommended products based on our algorithm:

| Product Name | Price (USD) |
|-------------|----------|
| IFB Neptune VX Free Standing 12 Place Settings Dishwasher | $423.39 |
| IFB Neptune SX1 Free Standing 15 Place Settings Dishwasher | $489.39 |
| Voltas Beko DF14W Free Standing 14 Place Settings Dishwasher | $347.49 |
| TP-Link TL-WA850RE(IN) 300 Mbps WiFi Range Extender | $16.16 |
| Hold up Triangle Shape Mobile Holder For Table | $1.50 |
| Airtel Regular Digital TV DTH Remote Compatible | $2.37 |
| KENT 16079 - Wet Grinder (White) | $54.99 |
| Google Chromecast 3 Media Streaming Device | $29.16 |
| Google Nest Hub (2nd gen), Display with Google Assistant | $76.99 |
| Butterfly Rapid Plus Wet Grinder with Coconut Scraper | $46.19 |

## Applications
This sentiment-enhanced recommendation system can help e-commerce platforms improve customer satisfaction by recommending products that genuinely resonate with users, potentially increasing conversion rates and reducing return frequencies.

## Technologies
Python, PyTorch, Transformers (BERT, RoBERTa), NLTK, Pandas, Matplotlib, Seaborn, HuggingFace

