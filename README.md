# Market Basket Analysis with Apriori Algorithm in Python

This project performs Market Basket Analysis using the Apriori algorithm to uncover associations between items bought together in a retail dataset. It uses the `apyori` library to generate association rules and identify frequent itemsets.

##  Overview

Market Basket Analysis is a key technique used in data mining to understand customer purchase behavior by finding associations between different items. This can be used for:
- Cross-selling strategies
- Recommendation engines
- Inventory optimization

In this notebook, we:
- Load and process transactional data
- Use the Apriori algorithm to discover strong association rules
- Sort the rules based on lift to find the most relevant item pairings

##  Dataset
- File: `Market_Basket_Optimisation.csv`
- Format: Each row represents one transaction with up to 20 items.
- Source: UCI Machine Learning Repository (or similar transaction data).

## Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `apyori`

## Apriori Parameters

```python
rules = apriori(
    transactions=transactions, 
    min_support=0.003, 
    min_confidence=0.2, 
    min_lift=3, 
    min_length=2, 
    max_length=2
)
