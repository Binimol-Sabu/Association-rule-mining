# 🛒 Market Basket Analysis using Apriori and FP-Growth

This project performs **Market Basket Analysis** on the **Groceries Dataset** using **Apriori** and **FP-Growth** algorithms to discover frequent itemsets and generate meaningful association rules. These rules help understand consumer purchase patterns — a vital task in retail analytics.

## 📁 Dataset Description

- **Source**: Groceries Dataset (transactional data)
- **Columns**:
  - `Member_number`: Unique customer ID
  - `Date`: Transaction date
  - `itemDescription`: Item purchased

Dataset contains **38,765 records** with **167 unique items**.

## 📊 Objectives

- Preprocess transactional data into a format suitable for market basket analysis.
- Apply **Apriori** and **FP-Growth** algorithms to find frequent itemsets.
- Generate and evaluate **association rules** based on confidence and lift.
- Compare insights from both algorithms.

## 🛠️ Libraries Used

- `pandas`
- `numpy`
- `matplotlib`, `seaborn`
- `mlxtend` (for Apriori, FP-Growth, and Association Rules)

## 🔍 Methodology

### 1. Data Preprocessing

- Grouped items by `Member_number` and `Date` to form transactions.
- Applied `TransactionEncoder` to convert transactions into a one-hot encoded format suitable for algorithm input.

### 2. Frequent Itemset Mining

- **Apriori**:
  - Minimum support: `0.001`
  - Output: 750 frequent itemsets
- **FP-Growth**:
  - Minimum support: `0.001`
  - Output: 750 frequent itemsets

### 3. Association Rule Generation

- Metric: **Confidence** (≥ 0.1)
- Evaluated rules using:
  - **Confidence**
  - **Lift**
  - **Support** etc.
 

### 4. Insights

- Top products: `whole milk`, `other vegetables`, `rolls/buns`, `soda`, `yogurt`
- Strongest rules (by confidence and lift):
  - `{sausage, yogurt} → whole milk`
  - `{rolls/buns, sausage} → whole milk`
- `whole milk` frequently appears as a consequent, indicating it's a high-utility cross-sell product.


## 🔚 Conclusion

This analysis provides valuable insight into customer purchase behavior. The derived rules can assist businesses in:
- Designing combo offers
- Product placement strategies
- Increasing average cart value



