# DSA Project Documentation
My name is `Ngbede Frank Ajo`. This is the first test of my ability as a Data Analyst. I want to say a big thank you to `The Incubator Hub` and 
the entire `DSA Team` for this life changing experience, and my wonderful, impactful and friendly Facilitators
`(Mr. Temidayo DeeTee, Mr. Femi Ayodele and Mr. Muhsin Hameed)` for their wonderful impact in my journey.

My special thank goes to my Father in The Lord, `Daddy G.O` who made this program possible for me to enjoy free of charge. 
May Almighty continue to bless protect you. We love you…

---

# 🛒 Amazon Product Review Analysis

## 📌 Introduction
This project explores and analyzes Amazon product reviews to uncover insights about customer behavior, product performance, and pricing strategies. 
Using Excel and data visualization techniques, it answers key business questions that can inform better product decisions and improve customer engagement.

---

## ❓ Problem Statement
Amazon’s vast product listings and inconsistent review data make it difficult to:
- Identify top-performing products
- Understand customer satisfaction
- Evaluate pricing effectiveness

This limits informed decision-making for both buyers and sellers.

---

## 🎯 Project Objectives 
- Identify top-rated and most-reviewed products  
- Understand the relationship between ratings and discount levels  
- Track customer feedback trends across categories
- Analyze the distribution of product prices 
- Build a clean, interactive Excel dashboard  

---

## 📊 Data Source & Description
The dataset was scraped from Amazon product pages and contains:
- **Product Details**: name, category, price, discount, and ratings  
- **Customer Engagement**: user reviews, titles, and content  

Each row represents a unique product, with reviewer data stored as comma-separated values.

---

## 🛠 Tools Used

- **Excel**: Data cleaning, calculated columns, Pivot Tables  
- **Charts**: Data visualization for rating, discount, and pricing patterns

--- 

## 🧹 Data Cleaning & Preparation
Here’s the step-by-step cleaning process:

- **Backup Original Data**: Created a copy of the original dataset for reference.
- **Removed Duplicates**: Dropped rows with duplicate `Product_ID`s.
- **Handled Missing Values**: Filled two missing `Rating_Count` entries using the column average.
- **Formatted Headers**: Capitalized headers using `=PROPER()` and Paste Special.
- **Split Category Column**: Used `Text to Columns` with delimiter `|` to split subcategories.
- **Dropped Irrelevant Columns**: Removed unnecessary columns like `img_link`, `user_name`, `review_title`, `about_product`, etc.

---

## 🔍 Exploratory Data Analysis (EDA)

To answer specific business questions, several calculated columns were created:

- **`Discount_Above50%`**:  
  `=IF(F2>=0.5, 1, 0)` → Flags products with ≥50% discount.

- **`Potential_Revenue`**:  
  `=Actual_Price × Rating_Count` → Used to estimate potential earnings.

- **`Price_Range`**:  
  Bucketed prices using:  
  `=IF(E2<200, "<₹200", IF(E2<500, "₹200–₹500", IF(E2<1000, "₹501–₹1000", ">₹1000")))`

- **`Product<1000_Review`**:  
  `=IF(H2<1000, 1, 0)` → Filters products with fewer than 1,000 reviews.

- **`Rating_Score`**:  
  `=G2 * H2` → Used to identify top products based on both rating and review volume.

---

## 📌 Key Business Questions Answered

1. **How many products have a discount of 50% or more?**  
   → Flagged using `Discount_Above50%`.

2. **What is the total potential revenue by category?**  
   → Summed `Potential_Revenue` in Pivot Table grouped by `Category`.

3. **How many unique products fall within defined price ranges?**  
   → Used `Price_Range` column and counted unique products via Pivot.

4. **How many products have fewer than 1,000 reviews?**  
   → Counted products using the `Product<1000_Review` flag.

5. **Top 5 products by combined rating and review count?**  
   → Sorted `Combined_Rating×R-Count` in Pivot Table.

6. **How does the rating relate to the level of discount?**  
   → Found that average ratings slightly decrease as discount increases.

   [Download Project File](https://github.com/frankajo/Amazon-Product-Review-Analysis/blob/main/Amazon%20case%20study_myProject.xlsx")

   [Dashboard](https://github.com/frankajo/Amazon-Product-Review-Analysis/blob/main/dashboard1.png)
   [Dashboard](https://github.com/frankajo/Amazon-Product-Review-Analysis/blob/main/dashbaord2.png)

---

## 🔍 Key Insights

- ⭐ **Average rating drops as discount increases**  
  Products with <10% discount received the highest average rating (4.21), while those with >50% had the lowest (4.05).
- No direct correlation between **discounts** and **customer ratings**
- 📦 **Electronics dominate in review volume**, but personal care products often yield higher profit margins.
- - Over **60%** of products are priced above ₹1000

![dashboard1](https://github.com/user-attachments/assets/66b2731a-e278-4254-931c-1778f9569ac7)
![dashbaord2](https://github.com/user-attachments/assets/32100073-7e07-4160-94fa-7e4d378cb795)


---

## ✅ Recommendations

- Offer **moderate discounts (10–20%)** to maintain good ratings while encouraging sales.  
- Focus on **inventory management** for top-rated, high-review products.

---

## ⚠️ Limitations

- Data may not reflect **seasonal or promotional trends**.  
- Reviews might be **biased or manipulated** (e.g., fake or incentivized).  

---

## 🧾 Conclusion

Analyzing Amazon product reviews helps sellers make informed decisions on pricing, inventory, and customer engagement strategies. 
By uncovering patterns in review behavior, sellers can gain a competitive edge in an overcrowded marketplace.

---



