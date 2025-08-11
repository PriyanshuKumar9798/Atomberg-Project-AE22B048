# Atomberg-Project-AE22B048

# AI Agent for Smart Fan Market Share of Voice Analysis

## Overview
This project is an AI-powered assistant that automatically searches Google for smart fan-related content, scrapes the pages, analyzes brand mentions, and calculates **Share of Voice (SoV)** and **Share of Positive Voice** for Atomberg and its competitors.

**Workflow:**
1. Looks up specific smart fan-related queries on Google.
2. Collects the top results and visits each page.
3. Detects brand mentions, topics being discussed, and sentiment (positive or negative).
4. Weighs results based on recency and sentiment strength.
5. Calculates SoV metrics.
6. Saves everything in a clean CSV file.

---

## Tech Stack
- **Python 3.9+** – main programming language  
- **Google Custom Search API** – to programmatically search Google  
- **Requests** – HTTP requests for APIs and webpages  
- **BeautifulSoup** – HTML parsing and text extraction  
- **dateutil** – date parsing  
- **difflib** – near-duplicate detection  
- **HuggingFace Transformers** – AI sentiment & topic classification  
- **CSV module** – for structured output  

---

## N Justification
We set **N = 50** results per query.  
- Lower N (like 10) may miss important mentions across blogs, news, and review sites.  
- Higher N (like 100) risks many duplicates and API rate limits.  
- **50 strikes a balance** between coverage and efficiency.

---

## Queries Used
1. Atomberg smart fan review  
2. Havells smart fan review  
3. Atomberg vs Havells smart fan  
4. Atomberg vs Crompton smart fan  
5. best smart ceiling fan in India  
6. most energy efficient smart fan in India  

---

## How We Covered the Analysis
- Mentions in posts/comments for Atomberg vs competitors  
- Engagement for posts that mention Atomberg vs competitors  
- Sentiment analysis to calculate Share of Positive Voice  

---

## Formulas
**Count-based SoV:**
\[
SoV = \frac{\text{Brand Mentions}}{\text{Total Mentions}} \times 100
\]

**Weighted SoV (Sentiment + Recency):**
\[
SoV_{weighted} = \frac{\text{Sum of Weights for Brand}}{\text{Total Weights}} \times 100
\]
where  
Weight = (1 + sentiment_score) × recency_decay

**Share of Positive Voice:**
\[
SoV_{positive} = \frac{\text{Positive Mentions for Brand}}{\text{Total Positive Mentions}} \times 100
\]

---

## Recommendations for Atomberg
1. Leverage high sentiment in "energy efficiency" topics for brand positioning.  
2. Target comparison content with Havells — the highest competing share.  
3. Create more content in high-engagement topics like "smart features" and "price/value".  
4. Monitor and address negative sentiment in durability-related reviews.  


