# 🛒 Market Basket Analysis

Analyzing 7,500+ retail transactions to discover product association patterns
using the Apriori and FP-Growth algorithms. Generates actionable rules for 
product bundling and recommendation systems.

## Key findings

| Rule | Confidence | Lift |
|------|-----------|------|
| herb & pepper → ground beef | 32.3% | 3.29x |
| escalope → pasta | 37.3% | 4.70x |
| light cream → chicken | 29.1% | 4.84x |
| cooking oil → spaghetti | 57.1% | 3.28x |
| shrimp → pasta | 32.2% | 4.51x |

> Lift > 3 means these items are bought together 3x more than by chance — 
> strong signal for cross-promotion or shelf placement.

## What is Market Basket Analysis?

A data mining technique used by retailers (Amazon, Flipkart, grocery stores) 
to find items frequently bought together. Powers the "frequently bought together" 
and "customers also bought" features.

- **Support** — how often an itemset appears in all transactions
- **Confidence** — how often the rule is correct (X bought → Y bought)
- **Lift** — how much more likely Y is bought with X vs. independently (>1 = real association)

## Dataset

- 7,501 transactions from a French retail store over one week
- Source: [Kaggle](https://www.kaggle.com/datasets/merged-retail-store)

## Implementation

Two approaches compared:

| Library | Algorithm | Notes |
|---------|-----------|-------|
| `apyori` | Apriori | Simple, slower on large datasets |
| `mlxtend` | Apriori + FP-Growth | Faster, more control over parameters |

## How to run

```bash
pip install numpy pandas matplotlib apyori mlxtend
jupyter notebook
```


Open either notebook and run all cells.

## Project structure


Market-basket-analysis/
├── Market Basket Analysis Using apyori package.ipynb
├── Market Basket Analysis Using mlxtend package.ipynb
├── Data/
│   └── store_data.csv
└── README.md

## Tech stack

Python · Pandas · NumPy · Matplotlib · Apyori · MLxtend
