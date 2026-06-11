# Amazon Skincare Reviews — Sentiment, Credibility & Negativity Bias Analysis

**MSc Business Analytics Dissertation | University of Bristol | August 2025**

[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)](Amazon_reviews_Skincare.ipynb)
[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)](Amazon_reviews_Skincare.ipynb)
[![NLP](https://img.shields.io/badge/NLP-DistilBERT-green)](Amazon_reviews_Skincare.ipynb)
[![License](https://img.shields.io/badge/License-Academic-lightgrey)]()

---

## Overview

This project investigates **how sentiment, credibility cues, and negativity bias in online reviews influence consumer trust and purchase intent** in the skincare industry. Using a mixed-method approach combining primary survey data and secondary Amazon review data, the study bridges attitudinal consumer perceptions with real-world behavioural outcomes.

The research is grounded in the **Elaboration Likelihood Model (ELM)** and extends existing eWOM (electronic word-of-mouth) theory into the underexplored skincare domain.

---

## Research Questions

1. Does review sentiment (valence) align with star ratings in online skincare reviews?
2. How do credibility cues such as verified purchase status affect consumer trust and helpfulness?
3. Does review detail (length) increase perceived credibility, and is this moderated by purchase frequency?
4. How does negativity bias manifest in online skincare reviews, and is it amplified by credibility cues?

---

## Methodology

### Dual Dataset Design

| Dataset | Type | Size | Source |
|---|---|---|---|
| Consumer Survey | Primary | 307 responses | Microsoft Forms — UK consumers |
| Amazon Reviews | Secondary | 2,012 reviews | McAuley Lab, UC San Diego |

### Analytical Approach

- **Sentiment Analysis** — DistilBERT transformer model (scores from −1 to +1)
- **Descriptive Statistics** — Distribution analysis, skewness, kurtosis
- **Pearson Correlation Analysis** — Construct validity across both datasets
- **OLS Regression with Moderation** — Interaction effects between credibility cues, sentiment, and consumer behaviour
- **Interaction Plots** — Visualising moderation effects across variable levels

---

## Key Findings

### H1 — Sentiment & Star Ratings ✅ Supported
Positive textual sentiment strongly predicts higher star ratings (B = 0.927, R² = 0.441). Review sentiment and ratings are highly consistent, validating automated NLP measures as reliable proxies for consumer satisfaction.

### H2 — Verified Purchase & Helpfulness ✅ Partially Supported
Review reliance is a strong predictor of trust in verified reviews (B = 0.417, p < .001). Verified purchase status significantly boosts helpfulness votes on Amazon (B = 0.409, p < .001), but the interaction with star ratings was not significant — suggesting consumers apply an additive rather than interactive credibility heuristic.

### H3 — Review Detail & Trust ✅ Strongly Supported
Review length significantly predicts both trust (survey) and helpfulness (Amazon). The interaction between verified purchase and review length was significant (B = 0.100, p = .001) — detailed verified reviews attract substantially more helpfulness votes than short or unverified ones.

### H4 — Negativity Bias ✅ Conditionally Supported
Negativity bias is present but conditional. Consumers who rely heavily on reviews show greater sensitivity to negative content (B = 0.445, p < .001). On Amazon, negativity alone was not significant — its impact was amplified specifically when reviews were both verified and detailed, confirming that **credibility cues strengthen negativity bias**.

## Data Sources

### Primary Data
- **Consumer Survey** — 307 anonymous UK respondents collected via Microsoft Forms (July–August 2025)
- Variables: Review reliance, trust in verified reviews, trust in detailed reviews, sensitivity to negative reviews, age, purchase frequency

### Secondary Data
- **Amazon Product Reviews** — McAuley Lab, University of California San Diego
- Dataset: [All Beauty Reviews](https://amazon-reviews-2023.github.io/) (1996–2023)
- Variables used: Review text, star rating, helpfulness votes, verified purchase status, review length
- Note: Raw `.jsonl` files excluded from repo due to size (311MB + 203MB). The processed dataset `merged_reviews_with_metadata.csv` is included.

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core analysis |
| DistilBERT | Sentiment analysis (NLP) |
| Pandas / NumPy | Data manipulation |
| Scikit-learn | Regression modelling |
| Matplotlib / Seaborn | Visualisation & interaction plots |
| Google Colab | Notebook environment |

**Google Colab Notebook:** [View on Colab](https://colab.research.google.com/drive/1FBJgK83H_9juQ7r3CDWUVZ33iSv4xTN?usp=sharing)

---

## Theoretical Framework

This study extends the **Elaboration Likelihood Model (Petty & Cacioppo, 1986)** to online review contexts:

- **Central route cues** — Sentiment valence, review detail/length, message quality
- **Peripheral route cues** — Verified purchase badges, helpfulness votes
- **Key finding** — Cues can interact; detailed verified reviews engage both routes simultaneously, making them disproportionately influential on consumer decisions

---

## Practical Implications

- **Platforms** should highlight verified, detailed reviews and use sentiment summaries to help consumers process information efficiently
- **Brands** should respond proactively to verified negative reviews, which are shown to be the most damaging credibility combination
- **Marketers** can use review reliance as a segmentation variable to target high-reliance consumers with credibility-signal-rich content

---

## Academic Context

> **Dissertation Title:** The Impact of Sentiment, Credibility and Negativity Bias in Online Reviews on Consumer Trust and Purchase Intent in the Skincare Industry
>
> **Degree:** MSc Business Analytics — University of Bristol Business School
>
> **Supervisor:** Dr Tian Han, School of Management
>
> **Word Count:** 11,214 | **Submitted:** August 2025

---

## Author

**Gokul Kumar**
MSc Business Analytics, University of Bristol (Distinction)

