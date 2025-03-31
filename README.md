# Customer Satisfaction Analysis Report  
**QuickService Retail Corp**  

---

## Table of Contents  
1. [Project Name](#project-name)  
2. [Project Background](#project-background)  
3. [Project Goals](#project-goals)  
4. [Data Structure & Initial Checks](#data-structure--initial-checks)  
5. [Executive Summary](#executive-summary)  
6. [Insights Deep Dive](#insights-deep-dive)  
7. [Recommendations](#recommendations)  
8. [Technical Details](#technical-details)  
9. [Assumptions and Caveats](#assumptions-and-caveats)  

---

## Project Name  
**QuickService Retail Corp: Branch Customer Satisfaction Comparison**  
Analysis of satisfaction scores across three retail branches (A, B, C) to identify performance trends and operational parity.  

---

## Project Background  
**Company Overview:**  
QuickService Retail Corp operates in the consumer retail sector, with 100+ branches nationwide since 2010. Key metrics include customer satisfaction scores (1-10 scale), average transaction time, and retention rates.  

**Data Context:**  
- **Dataset:** 20 customers rated all three branches (60 total responses) in Q3 2023.  
- **Analyst Role:** Determine statistical differences in satisfaction scores to guide resource allocation and service standardization.  

---

## Project Goals  
1. **Statistical Parity Check:** Use Kruskal-Wallis and post-hoc tests to compare branch performance.  
2. **Operational Benchmarking:** Identify outliers or trends impacting satisfaction consistency.  
3. **Strategic Alignment:** Provide data-driven recommendations for branch managers.  

**Key Focus Area:**  
- **Category:** Statistical significance of branch differences.  

---

## Data Structure & Initial Checks  
**Dataset:** `Customer Satisfaction.csv` (20 rows × 4 columns).  

**Columns:**  
- `Customer_ID`: Unique identifier (1–20).  
- `Branch_A`, `Branch_B`, `Branch_C`: Satisfaction scores (6–9 scale) for each branch.  

**Initial Checks:**  
- **Completeness:** 0 missing values across all columns.  
- **Ranges:** Scores clustered between 6–9 (min=6, max=9).  
- **Central Tendency:** Near-identical means (7.5–7.55) and low variability (std. dev. ~1.1).  

---

## Executive Summary  
**Top Insights:**  
1. **No Statistical Differences:**  Kruskal-Wallis (*p=0.99*) confirm parity across branches.  
2. **Consistent Performance:** All branches scored mean ~7.5/10, reflecting uniform service quality.  

---

## Insights Deep Dive  
**Statistical Significance:**  
1. **Normality Check (Shapiro-Wilk):**  
   - All branches violated normality (*p < 0.05*), necessitating non-parametric tests.  
2. **Kruskal-Wallis Test:**  
   - *H-statistic = 0.02, p=0.99* – No significant differences.  


---

## Recommendations  
1. **Centralized Training Programs:** Maintain uniformity by sharing best practices across branches.  
2. **Expand Sample Size:** Collect data from 50+ customers per branch to detect subtle differences.  
3. **Qualitative Feedback:** Add open-ended survey questions to contextualize numerical scores.  
4. **Quarterly Re-Analysis:** Track trends seasonally to identify emerging gaps.  

---

## Technical Details  
**Tools:**  
- **Python:** `pandas` (data wrangling), `pingouin` (hypothesis testing), `scipy` (normality/variance checks).  
- **Tests:** Shapiro-Wilk (normality), Levene (variance), Kruskal-Wallis (group differences).  

**Rationale:**  
- Non-parametric tests prioritized due to non-normal data and small sample size.  
 

---

## Assumptions and Caveats  
1. **Independence Assumption:** Treated branches as independent groups, but customers rated all three (potential pseudoreplication).  
2. **Small Sample Size:** 20 customers per branch limits power to detect subtle differences.  
3. **Timeframe Limitation:** Data reflects a single quarter; seasonal variations unaccounted for.  
4. **Scale Restriction:** Scores capped at 6–9, reducing variability.  

--- 

**Conclusion:**  
Branches A, B, and C demonstrate statistically indistinguishable satisfaction scores. Strategic focus should shift to enhancing overall service quality rather than inter-branch comparisons.  
