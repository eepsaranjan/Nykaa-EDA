# Nykaa-EDA
EDA on Nykaa product data — uncovering pricing, rating, and brand performance insights using Python &amp; Pandas.
# Nykaa Product Catalog: Exploratory Data Analysis

Exploratory Data Analysis of Nykaa's product catalog (610 products) examining pricing, ratings, brand performance, and category trends. Identifies key pricing-quality mismatches and actionable business insights using Python, Pandas, Matplotlib, and Seaborn.

## 📋 Problem Statement

Nykaa hosts a large catalog of beauty and personal care products across multiple brands and categories. This project analyzes 610 Nykaa products to understand patterns in pricing, ratings, reviews, categories, and brands — with the goal of identifying pricing-quality mismatches and flagging categories or brands that may need attention.

## 🎯 Business Objective

To use exploratory data analysis to determine:
1. How pricing is distributed across the catalog, and what that says about market positioning.
2. Whether price influences customer rating, or if the two are unrelated.
3. Which categories/brands perform best or worst in ratings, and where reputational risks exist.
4. How customer engagement (reviews) relates to price and category.

## 🛠️ Tools & Libraries Used

- **Python 3**
- **Pandas** — data cleaning and manipulation
- **Matplotlib** & **Seaborn** — data visualization
- **Google Colab / Jupyter Notebook** — analysis environment

## 📊 Dataset

- **Source:** Nykaa Product Review dataset (`Nykaa_Product_Review.csv`)
- **Original size:** 625 rows × 18 columns
- **After cleaning:** 610 rows × 17 columns
- **Key columns:** Product Name, Brand, Category, Price, Rating, Reviews Count, Market, Currency

## 🧹 Data Cleaning Highlights

- Converted `Product Price` and `Product Rating` from text to numeric using `pd.to_numeric(errors='coerce')`
- Dropped 15 rows with corrupted/unusable price values
- Created a simplified `Main Category` column from the nested category path
- Handled missing values with context-appropriate fills (e.g., `0` for unrated products, `"Not Specified"` for missing categories)
- Removed irrelevant internal metadata columns (`Expected Category Count`, `Expected Brand Count`)

## 🔍 Key Findings

- **Price does not predict rating** — correlation is nearly zero (-0.09)
- The catalog is dominated by **affordable products (₹0–500)**, which also have the **highest ratings and engagement**
- **Products priced ₹1000–2000** show a noticeable rating dip
- **High-priced Skin products** specifically underperform in ratings
- **Inner Sense**, the priciest top-10 brand, has the lowest ratings overall — driven almost entirely by its **Mom & Baby line (~0.4 rating)**
- Expensive products consistently receive **far fewer reviews**, suggesting a trust/visibility gap rather than low demand
- Categories like **Mom & Baby, Health & Wellness, and Appliances** have too few products for reliable conclusions
- **Himalaya and Biotique** are the most consistent, reliably well-rated brands across categories

## ✅ Recommendations

1. Fix Inner Sense's Mom & Baby line urgently — extremely low rating despite high price
2. Review premium Skin products (₹1000+) for quality issues
3. Run review-generation campaigns for expensive products
4. Continue investing in the budget segment (₹0–500)
5. Expand thin categories (Mom & Baby, Wellness, Appliances) before trusting their ratings
6. Treat pricing and quality as separate business levers
7. Prioritize consistent brands like Himalaya and Biotique for partnerships

## 📁 Project Structure

```
├── Nykaa_EDA_Capstone.ipynb   # Main analysis notebook
├── Nykaa_Product_Review.csv   # Dataset
└── README.md                  # Project overview
```

## 🚀 How to Run

1. Clone this repository
2. Open `Nykaa_EDA_Capstone.ipynb` in Jupyter Notebook or Google Colab
3. Ensure the dataset CSV is in the same directory (or update the file path)
4. Run all cells sequentially
