# Wine Review Analytics: Telling a Story with Data

## Overview
Wine pricing and ratings are often treated as indicators of quality, but these signals can be subjective, inconsistent, and influenced by hidden factors.

This project explores a large-scale wine review dataset to uncover how flavor language, geographic origin, and reviewer bias affect wine ratings and pricing.

Using exploratory data analysis, text analysis, and statistical comparisons, we identify meaningful patterns that help consumers make better purchasing decisions and help producers/retailers better position their products.

---

## Problem Statement
Consumers often assume:

- expensive wine = better wine
- famous wine regions = highest quality
- review scores are objective

This project investigates whether these assumptions hold true.

Core questions explored:

1. Which flavor descriptors are associated with higher wine ratings and prices?
2. Do famous wine-producing countries consistently produce the highest-rated wines?
3. How much reviewer bias affects wine scores?

---

## Business / Stakeholder Value

### Consumers
Helps buyers make smarter wine purchasing decisions by showing:

- price does not always reflect quality
- certain flavor profiles consistently align with stronger reviews
- reviewer subjectivity impacts ratings

### Retailers / Sellers
Supports inventory and marketing decisions by identifying:

- high-performing flavor profiles
- undervalued regions
- pricing inefficiencies

### Producers / Wineries
Provides insight into:

- market preferences
- flavor positioning
- how reviewer behavior may influence perceived quality

---

## Dataset

### Source
Wine Reviews Dataset (Kaggle)

Dataset:
https://www.kaggle.com/datasets/zynicide/wine-reviews

### Dataset Details
- ~130,000 wine reviews
- Multiple countries and regions
- Structured + unstructured data

Key columns:
- country
- province
- region
- price
- points
- description
- variety
- taster_name

---

## Methodology

### Data Cleaning
Performed preprocessing using Polars:

- removed null/incomplete records
- standardized regional fields
- combined region_1 / region_2
- cleaned text descriptions
- removed irrelevant columns

---

### Exploratory Analysis
Investigated:

- price distributions
- review score distributions
- region performance
- flavor descriptor frequency

---

### NLP / Text Analysis
Extracted recurring flavor phrases from review descriptions.

Examples:
- black cherry
- black pepper
- black fruit
- red berry
- black currant

Used phrase frequency and aggregated score comparisons.

---

### Reviewer Bias Analysis
Calculated adjusted wine scores by comparing:

reviewer average score vs global average score

This isolates reviewer tendencies and highlights scoring bias.

---

## Key Findings

### 1. Flavor language strongly predicts pricing and ratings
Dark fruit and spice descriptors (e.g., black cherry, black pepper) are associated with stronger scores and higher pricing.

---

### 2. Famous regions do not always produce the highest-rated wines
Smaller niche wine regions frequently outperform globally recognized regions.

This challenges assumptions around prestige-based purchasing.

---

### 3. Reviewer bias is measurable
Some tasters consistently score above or below baseline averages.

This means wine ratings should not always be interpreted as purely objective measures.

---

## Tools Used
- Python
- Polars
- Jupyter Notebook
- Matplotlib
- NumPy

---

## Repository Structure

```bash
wine-review-analytics/
│
├── Final_Report.ipynb
├── README.md
├── requirements.txt
└── data/
