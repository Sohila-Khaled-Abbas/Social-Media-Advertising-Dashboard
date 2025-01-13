# Social Media Advertising Dashboard

## Description
This repository contains a **comprehensive Power BI dashboard** for analyzing social media advertising campaigns. It includes data cleaning with Python, exploratory visualizations, and a multi-page Power BI dashboard focusing on campaign performance, audience engagement, and channel effectiveness. The dashboard is designed to analyze campaign performance, audience engagement, and channel effectiveness based on data from January 2022 to December 2022. It provides actionable insights for marketers, analysts, and decision-makers to optimize advertising strategies.

## Features

### 1. Data Cleaning Using Python
- Cleaned the dataset with Python (`pandas`, `numpy`).
- Key steps:
  - Filled missing ROI values with the mean.
  - Converted `Acquisition_Cost` to a numeric format.
  - Created a new feature: `Total_Spend` (Clicks × Acquisition_Cost).
  - Converted the `Date` column to datetime format.
  - Exported cleaned data for Power BI integration.

---

### 2. Power BI Dashboard
#### 1. **Campaign Overview**
- **Key Visualizations:**
  - **Total Campaigns:** 300,000 campaigns analyzed.
  - **Total Acquisition Cost:** $2.3 billion.
  - **Top Segment:** Health.
  - **ROI Trend:** Average ROI of 3.18, with trends from January 2022 to December 2022.
  - **Top 5 Companies by ROI:** Attire Artistry, Balance Beam, Culinary Quest, Space Spruce, and Style Sphere.
  - **Campaign Distribution by Customer Segment:** Health (19.98%), Home (20.03%), Food (19.98%), Fashion (20.02%), Technology (20.02%).

![Campaign Overview](Screenshots/campaign_overview.png)

---

#### 2. **Campaign Performance Analysis**
- **Key Visualizations:**
  - **Total Clicks:** 5 billion.
  - **Total Impressions:** 17 billion.
  - **Total Conversions:** 436.01 million.
  - **Top Spender:** Space Spruce ($1.15 trillion).
  - **Distribution of Campaign Goals:** Brand Awareness (75,248 campaigns), Increase Sales, Market Expansion, Product Launch.
  - **ROI by Company:** Attire Artistry had the highest ROI (323.46%).

![Campaign Performance](Screenshots/campaign_performance.png)

---

#### 3. **Audience Segmentation and Engagement**
- **Key Visualizations:**
  - **Total Target Audience Reached:** 300,000.
  - **Most Popular Campaign Goal:** Brand Awareness.
  - **Location with Highest ROI:** New York.
  - **Average Engagement Score:** 4.37.
  - **Engagement Score Over Months:** Peaked from December 2022 to January 2022 (10.00).
  - **Target Audience by Campaign Goal:** Women 18-24 (33.6%), Men 25-34 (23.8%), Women 25-34 (23.8%).

![Audience Segmentation](Screenshots/audience_segmentation.png)

---

#### 4. **Channel Performance Comparison**
- **Key Visualizations:**
  - **Total Impressions:** 17 billion (Facebook: 4.4 billion, Instagram: 3.0 billion, Twitter: 2.0 billion, Pinterest: 1.58 billion).
  - **Total Clicks:** 5 billion (Facebook: 1.52 billion, Instagram: 1.52 billion, Twitter: 1.52 billion, Pinterest: 0.85 billion).
  - **Total Conversions:** 436.01 million.
  - **Total Spend Across Channels:** $55 trillion.
  - **Top Performer:** Facebook (1.52 billion clicks).

![Channel Performance](Screenshots/channel_performance.png)

---

## Files Included
- **Dashboard.pbix:** Power BI file with the full dashboard.
- **Dataset.csv:** Cleaned data source used in the dashboard.
- **Documentation.md:** Step-by-step guide on how to use and customize the dashboard.

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/sohilakhaledabbas/social-media-advertising-dashboard.git
   ```
2. Open the `Dashboard.pbix` file in Power BI Desktop.
3. Explore the pages and interact with the visualizations.

## Insights Derived
- Campaign ROI analysis by company.
- Audience engagement trends over time.
- Channel effectiveness comparison.
- Geographical distribution of campaign performance.

## Tools & Technologies
- Python: pandas, numpy, matplotlib, seaborn
- Power BI: Interactive dashboard design
- Dataset: [Social Media Advertising Dataset on Kaggle](https://www.kaggle.com/datasets/jsonk11/social-media-advertising-dataset/data)

---

## Python Code for Data Cleaning
```python
# Import necessary libraries
import pandas as pd
import numpy as np

# Load the dataset
file_path = r"Social_Media_Advertising.csv"
df = pd.read_csv(file_path)

# Data Cleaning
df['ROI'].fillna(df['ROI'].mean(), inplace=True)
df['Acquisition_Cost'] = df['Acquisition_Cost'].replace('[\$,]', '', regex=True).astype(float)
df['Date'] = pd.to_datetime(df['Date'])
df['Total_Spend'] = df['Acquisition_Cost'] * df['Clicks']

# Save the cleaned dataset
df.to_csv("Social_Media_Advertising_Cleaned.csv", index=False)
```
---
## Feedback

If you have any suggestions or feedback, feel free to open an issue or connect with me on [LinkedIn](www.linkedin.com/in/sohilakhaledabbas).

---

## Future Enhancements
- Integration with live data sources.
- Advanced machine learning insights using Python/R integration.
- Adding more custom visuals for deeper analysis.
---
## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

