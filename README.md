# A/B Testing for E-commerce Landing Page

## Project Overview

This project demonstrates an end-to-end A/B testing workflow on an e-commerce platform to evaluate whether a new landing page design improves conversion rates compared to the existing page. Using a dataset of ~290,000 users from Kaggle, we applied statistical testing to determine the impact of design changes and provided actionable product recommendations.

**Key Business Question:** Should the platform switch to the new landing page design to increase user conversions?

## Hypothesis

* **Null Hypothesis (H₀):** The new landing page does not improve conversion rates compared to the old page.
* **Alternative Hypothesis (H₁):** The new landing page improves conversion rates.

## Dataset & Tools

The dataset contains key user metrics including: user identifiers, landing page assignments, timestamps of visits, conversion outcomes, and user country. Additional data allows for segmentation analysis and validation of experimental groups.

**Tools & Libraries Used:**

* Python (Pandas, Numpy, SciPy, Matplotlib, Seaborn)
* Jupyter Notebook for exploration and visualization
* Statistical testing: Z-test and Chi-square test
* Business and product analysis methodologies

## Methodology

### 1. Data Preparation

* Merged user datasets with landing page information to create a complete experiment dataset.
* Removed duplicate user IDs to ensure accuracy.
* Verified that control group users were correctly assigned to the old page and treatment group users to the new page.
* Final dataset contained ~290,000 unique users.

  It contains the following key columns:  

- **user_id** → Unique identifier for each user.  
- **timestamp** → Date and time when the user visited the page.  
- **group** → Indicates whether the user was in the **control group** (saw the old page) or **treatment group** (saw the new page).  
- **landing_page** → Which page the user actually landed on (old_page or new_page).  
- **converted** → Binary variable (0/1) showing whether the user completed the desired action (conversion).  
- **country** (in a supplementary dataset) → User’s country, useful for segmentation analysis.  


### 2. Exploratory Analysis

* Calculated overall conversion rate: ~12%.
* Group-wise conversion rates: Control (Old Page) ~12.0%, Treatment (New Page) ~12.1%.
* Observed minimal differences in conversion, suggesting any difference may be due to random variation.

### 3. Statistical Testing

* **Z-test:** Computed Z-statistic of 1.29 and p-value of 0.195, failing to reject the null hypothesis.
* **Chi-square test:** Chi-square statistic of 1.66 with p-value of 0.197, also failing to reject the null hypothesis.

**Interpretation:** Both statistical tests indicate that the new design does not significantly improve conversion rates.

### 4. Segmentation Analysis

* Segmented conversions by **country** to explore geographic variation.
* Explored **time patterns** to ensure no temporal bias influenced results.
* Optional segmentation by **device type or traffic source** could further refine insights.

## Key Insights

* Conversion rates between the old and new landing page are nearly identical, confirming that the new design does not produce measurable gains.
* Minor observed differences are likely due to random chance.
* Existing page is stable and reliable; switching may not yield benefits and could risk introducing issues.

## Product Recommendations

Based on analysis, the recommended actions are as follows:

* **Retain the Old Landing Page:** Since conversion rates are similar, focus resources elsewhere for greater impact.
* **Iterate with Micro-Experiments:** Test specific elements such as call-to-action placement, color, and messaging to incrementally improve user engagement.
* **UX Improvements:** Refine visual hierarchy and ensure consistency in design elements to support clarity and user confidence.
* **Personalization Strategies:** Explore targeted banners or content based on user attributes like location, device, or behavior patterns to enhance conversion.
* **Monitor Metrics Continuously:** Track future experiments and funnel performance to quickly detect changes or anomalies.



## Future Product Experiments

* Evaluate the effect of CTA color and placement on first-click rate.
* Conduct personalized banner testing by country or user segment.
* Assess simplified copy on new user engagement to improve onboarding experience.
* Run micro A/B tests on checkout process elements to identify friction points.


