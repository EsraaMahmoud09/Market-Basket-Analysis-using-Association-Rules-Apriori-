# Market-Basket-Analysis-using-Association-Rules-Apriori-
"A data analysis project to find association rules between supermarket items using Apriori algorithm."

##  Market Basket Analysis — Interpretation, Insights & Recommendations

##  Project Overview

This project applies **Market Basket Analysis** using the **Apriori algorithm** and **Association Rules** to discover relationships between products in transaction data.

The main objective is to understand customer purchasing behavior and identify which products are frequently bought together to improve:
- Cross-selling strategies
- Store layout optimization
- Recommendation systems

---

##  Exploratory Data Analysis (EDA)

- A bar chart was created to visualize the **top 10 most frequent items**.
- **Whole Milk** is the most popular item, appearing in **18.2% of all transactions**.
- Other frequent items include:
  - Vegetables
  - Rolls/Buns (Bread)
  - Yogurt

 This indicates that **essential grocery items** are the main drivers of sales and appear in most customer baskets.

---

##  Association Rules Results

###  Generated Rules

| Antecedent           | Consequent     | Support  | Confidence | Lift  | Kulc  | MaxConf | AllConf | Jaccard | Chi-Square |
|---------------------|---------------|----------|------------|-------|-------|---------|---------|----------|------------|
| other vegetables    | whole milk    | 0.014837 | 0.121511   | 0.769 | 0.107 | 0.1215  | 0.0939  | 0.0559   | 0.001025   |
| rolls/buns          | whole milk    | 0.013968 | 0.126974   | 0.804 | 0.107 | 0.1270  | 0.0884  | 0.0550   | 0.000667   |
| soda                | whole milk    | 0.011629 | 0.119752   | 0.758 | 0.096 | 0.1198  | 0.0736  | 0.0478   | 0.000896   |
| yogurt              | whole milk    | 0.011161 | 0.129961   | 0.822 | 0.100 | 0.1300  | 0.0707  | 0.0480   | 0.000425   |

---

###  Key Observations

- All rules have **Lift < 1**, which indicates:
  - Weak or negative associations between products
  - No strong complementary relationship

- Confidence values range between **12% → 13%**:
  - Example: *If a customer buys yogurt → 13% chance they also buy whole milk*

- **Whole Milk dominates the results**:
  - Appears frequently in transactions
  - Drives confidence values higher

 Important Insight:
> High confidence does NOT necessarily mean strong relationship (it may be due to product popularity)

---

##  Heatmap Analysis

###  Lift Heatmap

- Measures the **true strength of association** between products

#### Key Insights:
- Strongest relationships:
  - Sausage ↔ Yogurt (Lift ≈ 1.11)
  - Sausage ↔ Soda
  - Yogurt ↔ Citrus Fruit

- Most values ≈ 1 or less:
  - Indicates weak relationships

- Whole Milk:
  - Low lift with most items
  - Acts as a **staple product**

 Conclusion:
> Lift reveals real product relationships beyond popularity

---

###  Confidence Heatmap

- Measures probability:  
  *If A is purchased → likelihood of B*

#### Key Insights:
- Whole Milk shows highest confidence values (0.11–0.15)
- Example:
  - Sausage → Whole Milk ≈ 15%

 Interpretation:
- Whole Milk appears frequently in baskets
- High confidence is driven by popularity, not strong association

---

##  Key Insights

###  1. Product Clusters Exist
- Sausage ↔ Yogurt  
- Sausage ↔ Soda  
- Yogurt ↔ Citrus Fruit  

 Indicates **meal-based purchasing behavior**

---

###  2. Whole Milk is a Dominant Product
- Appears in most baskets
- Inflates confidence values
- Has weak Lift relationships

 Insight:
> High frequency ≠ strong association

---

###  3. Lift is More Reliable than Confidence
- Confidence is affected by popularity
- Lift shows true relationships

---

###  4. Sparse Dataset Behavior
- Total Frequent Itemsets: **69**
- Maximum itemset size: **2**
- No 3-itemsets generated

 Meaning:
- Customers usually buy **small combinations**
- Strong multi-item relationships are rare

---

##  Apriori Algorithm Process
DATA (Transactions)
|
v
C1 (Candidate 1-itemsets)
|
v
F1 (Frequent 1-itemsets)
|
v
C2 (Candidate 2-itemsets)
|
v
F2 (Frequent 2-itemsets)
|
v
C3 (NOT generated )
|
v
 STOP

 
---

##  Final Results

- Total Frequent Itemsets: **69**
- Max Itemset Size: **2**
- No higher-order combinations found

---

##  Business Recommendations

###  1. Cross-Selling Strategy
- Place related products together:
  - Sausage ↔ Yogurt
  - Yogurt ↔ Citrus Fruits

---

###  2. Bundle Offers
- Sausage + Yogurt  
- Yogurt + Citrus Fruits  

 Increase basket size

---

###  3. Store Layout Optimization
- Arrange items based on association strength
- Encourage impulse buying

---

###  4. Recommendation System
- Sausage → Recommend Yogurt  
- Citrus Fruit → Recommend Yogurt  
- Soda → Recommend Sausage  

---

###  5. Marketing Strategy
- Focus on product relationships rather than individual product popularity when designing campaigns.
- Not just high-frequency items like Whole Milk

---

##  Final Conclusion

Market Basket Analysis shows that:

- Market Basket Analysis shows that customer purchasing behavior is driven more by product combinations than individual product popularity

 The most valuable insights come from:
**Lift-based relationships**, which reveal true associations and help improve:
- Sales strategies
- Product placement
- Recommendation systems

- ---


