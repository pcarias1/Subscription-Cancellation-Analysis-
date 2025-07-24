# Subscription Cancellation Analysis

# Executive Summary
Facing a significant churn issue and major revenue loss, company leadership sought deeper insights into the reasons behind subscription cancellations to guide retention strategy. This project analyzes user reported cancellation data collected through a three step form in the product workflow. Using SQL and data visualization tools, the analysis uncovered which reasons users selected, how many they chose, and how these trends shifted over time. These findings support actionable retention strategies and product experience improvements.

Key recommendations include:
1. Improving onboarding to better communicate product value
2. Enhancing support to address dissatisfaction before cancellation
3. Streamlining the cancellation process to improve feedback collection

# Business Problem
Leadership has noticed a spike in churn, significantly impacting revenue. The company’s analytics team does not currently have visibility into why users are leaving. The existing cancellation workflow includes a dropdown with one required reason and two optional reasons.
This project aims to:
* Determine how complete and trustworthy the cancellation reason data is
* Identify the most common reasons for churn
* Analyze how cancellation trends shift over time
* Provide recommendations to reduce churn and improve product-market fit

# Methodology
1. Used SQL to clean and restructure cancellation data from a wide format (3 columns) into a normalized long format using UNION ALL
2. Created binary indicators for each reason field to calculate average reasons selected per user
3. Analyzed cancellation reason frequency by position (1st, 2nd, 3rd)
4. Grouped reason trends by year to detect changes over time
5. Used data visualizations (bar charts, faceting) to support findings


# Skills & Tools

SQL:
* CTEs
* CASE statements
* Aggregations
* Union
* Window functions
* View creation

Tools:
* SQL / Snowflake
* Hex ( visualization)

Data Concepts:
* Funnel analysis
* Data normalization
* Categorical aggregation
* Trend analysis
* Exploratory Data Analysis (EDA)

# Results & Business Recommendations
Results
* 2.18 average reasons selected per subscription; 1.18 were optional beyond the required first reason.
* Most users selected "Expensive", "Not useful", and "Went to a competitor" as reasons for canceling.
* "Not useful" was the most frequent primary (1st) reason, suggesting users didn’t see value in the product.
* "Went to a competitor" was commonly chosen in the 2nd and 3rd positions, pointing to competitive pressure.
* Null values in the 3rd reason field were high, indicating form fatigue or low engagement.
* Over time, "Bad customer service" increased in frequency, particularly in 2024, signaling a growing pain point.

  ## Breakdown of Cancellation Reasons by Selection Order
<img width="966" height="437" alt="Screenshot 2025-07-24 at 6 23 50 PM" src="https://github.com/user-attachments/assets/d4ca534f-7683-47c4-8b45-c0a76a10c2ff" />

# Business Recommendations
1. Improve onboarding and early product education to address “Not useful” perceptions.
2. Add progress bar and confirmation messaging to the cancellation form to encourage completion of all reason fields.
3. Introduce exit prompts with discount offers for users who select "Expensive" as their reason.
4. Benchmark competitor offerings and price/value perceptions to reduce competitor driven churn.
5. Monitor reasons over time and align product roadmap with high volume concerns (e.g., documentation, bugs, pricing confusion).

# Next Steps
1. Test two versions of the cancellation process to see which one works better, such as different designs, messages, or wording.
2. Compare behavior of churned vs. retained users, especially around product usage and support interactions.
3. If we get written feedback from users, analyze the tone of their messages (whether they are happy, frustrated, or confused) to better understand their reasons for canceling. 
