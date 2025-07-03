# Optimizing Digital Ad Campaigns: A Data-Driven Case Study

## Project Overview

This project focuses on analyzing user ad exposure and conversion data to evaluate the effectiveness of a digital advertising campaign. Through detailed analysis and A/B testing techniques, the goal was to identify key drivers of conversion, understand user behavior patterns related to ad exposure, estimate potential revenue generation, and provide actionable recommendations for optimizing future marketing efforts.

## Table of Contents

- [Project Goal](#project-goal)
- [Dataset & Features](#dataset--features)
- [Tools Used](#tools-used)
- [Analysis Phases & Key Findings](#analysis-phases--key-findings)
  - [Phase 1: Data Understanding & Preprocessing](#phase-1-data-understanding--preprocessing)
  - [Phase 2: Exploratory Data Analysis (EDA)](#phase-2-exploratory-data-analysis-eda)
  - [Phase 3: Hypothesis Testing & A/B Testing](#phase-3-hypothesis-testing--ab-testing)
  - [Phase 4: Granular Performance - Day-Hour Interaction](#phase-4-granular-performance---day-hour-interaction)
  - [Phase 5: Potential Revenue Estimation](#phase-5-potential-revenue-estimation)
- [Key Recommendations](#key-recommendations)
- [Conclusion](#conclusion)

## Project Goal

The primary objectives of this analysis were to:
1.  **Analyze Experimental vs. Control Groups:** Determine the success of the ad campaign by comparing the "ad" group (experimental) to the "psa" group (control).
2.  **Assess Statistical Significance:** Use A/B testing techniques to statistically validate observed differences in conversion rates across various user segments and ad exposure patterns.
3.  **Identify Conversion Drivers:** Uncover specific days, hours, and total ad exposures that significantly influence user conversion.
4.  **Estimate Revenue Potential:** Project potential revenue generated from the ad campaign based on conversion success (with a clear assumption on revenue per conversion).
5.  **Provide Actionable Recommendations:** Offer data-backed strategies for optimizing future ad campaigns.

## Dataset & Features

The analysis was performed on a dataset containing user-level information related to ad exposure and conversion. Key features include:

* **`User ID`**: Unique identifier for each user.
* **`Test Group`**: Indicates whether the user was in the "ad" group (saw the advertisement) or the "psa" group (saw the public service announcement or nothing). This feature was crucial for the A/B test.
* **`Converted`**: Binary indicator (True/False) of whether the user bought the product.
* **`Total Ads`**: The total number of ads seen by the user.
* **`Most Ads Day`**: The day of the week when the user saw the highest number of ads.
* **`Most Ads Hour`**: The hour of the day (24-hour format) when the user saw the highest number of ads.

## Tools Used

* **Google Sheets**: Utilized for initial data overview and basic understanding of the dataset structure.
* **Google Colab**: The primary Python environment for data loading, preprocessing, exploratory data analysis, statistical testing, and visualization.
* **Python Libraries**: `pandas` (for data manipulation), `numpy` (for numerical operations), `matplotlib.pyplot` and `seaborn` (for data visualization), `statsmodels.stats.proportion` (for two-proportion Z-tests and confidence intervals).
* **Google Gemini**: Used for assistance in precise interpretations of charts, figures, and statistical outputs.

## Analysis Phases & Key Findings

### Phase 1: Data Understanding & Preprocessing

This initial phase involved loading the dataset, inspecting its structure, handling missing values, and ensuring data types were appropriate for analysis (e.g., `Converted` to boolean, `Total Ads` to numeric, and managing outliers in `Total Ads`).

### Phase 2: Exploratory Data Analysis (EDA)

EDA provided initial insights into the data distribution and relationships:
* **Overall Conversion Rates:** Established baseline conversion rates across different segments.
# Optimizing Digital Ad Campaigns: A Data-Driven Case Study

## Project Overview

This project focuses on analyzing user ad exposure and conversion data to evaluate the effectiveness of a digital advertising campaign. Through detailed analysis and A/B testing techniques, the goal was to identify key drivers of conversion, understand user behavior patterns related to ad exposure, estimate potential revenue generation, and provide actionable recommendations for optimizing future marketing efforts.

## Table of Contents

- [Project Goal](#project-goal)
- [Dataset & Features](#dataset--features)
- [Tools Used](#tools-used)
- [Analysis Phases & Key Findings](#analysis-phases--key-findings)
  - [Phase 1: Data Understanding & Preprocessing](#phase-1-data-understanding--preprocessing)
  - [Phase 2: Exploratory Data Analysis (EDA)](#phase-2-exploratory-data-analysis-eda)
  - [Phase 3: Hypothesis Testing & A/B Testing](#phase-3-hypothesis-testing--ab-testing)
  - [Phase 4: Granular Performance - Day-Hour Interaction](#phase-4-granular-performance---day-hour-interaction)
  - [Phase 5: Potential Revenue Estimation](#phase-5-potential-revenue-estimation)
- [Key Recommendations](#key-recommendations)
- [Conclusion](#conclusion)

## Project Goal

The primary objectives of this analysis were to:
1.  **Analyze Experimental vs. Control Groups:** Determine the success of the ad campaign by comparing the "ad" group (experimental) to the "psa" group (control).
2.  **Assess Statistical Significance:** Use A/B testing techniques to statistically validate observed differences in conversion rates across various user segments and ad exposure patterns.
3.  **Identify Conversion Drivers:** Uncover specific days, hours, and total ad exposures that significantly influence user conversion.
4.  **Estimate Revenue Potential:** Project potential revenue generated from the ad campaign based on conversion success (with a clear assumption on revenue per conversion).
5.  **Provide Actionable Recommendations:** Offer data-backed strategies for optimizing future ad campaigns.

## Dataset & Features

The analysis was performed on a dataset containing user-level information related to ad exposure and conversion. Key features include:

* **`User ID`**: Unique identifier for each user.
* **`Test Group`**: Indicates whether the user was in the "ad" group (saw the advertisement) or the "psa" group (saw the public service announcement or nothing). This feature was crucial for the A/B test.
* **`Converted`**: Binary indicator (True/False) of whether the user bought the product.
* **`Total Ads`**: The total number of ads seen by the user.
* **`Most Ads Day`**: The day of the week when the user saw the highest number of ads.
* **`Most Ads Hour`**: The hour of the day (24-hour format) when the user saw the highest number of ads.

## Tools Used

* **Google Sheets**: Utilized for initial data overview and basic understanding of the dataset structure.
* **Google Colab**: The primary Python environment for data loading, preprocessing, exploratory data analysis, statistical testing, and visualization.
* **Python Libraries**: `pandas` (for data manipulation), `numpy` (for numerical operations), `matplotlib.pyplot` and `seaborn` (for data visualization), `statsmodels.stats.proportion` (for two-proportion Z-tests and confidence intervals).
* **Google Gemini**: Used for assistance in precise interpretations of charts, figures, and statistical outputs.

## Analysis Phases & Key Findings

### Phase 1: Data Understanding & Preprocessing

This initial phase involved loading the dataset, inspecting its structure, handling missing values, and ensuring data types were appropriate for analysis (e.g., `Converted` to boolean, `Total Ads` to numeric, and managing outliers in `Total Ads`).

### Phase 2: Exploratory Data Analysis (EDA)

EDA provided initial insights into the data distribution and relationships:
* **Overall Conversion Rates:** Established baseline conversion rates across different segments.
* **Day and Hour Trends:** Preliminary observations showed potential variations in conversion rates based on the day of the week and hour of the day.
* **Impact of Total Ads:** A clear trend emerged indicating higher conversion rates with increased ad exposure.

### Phase 3: Hypothesis Testing & A/B Testing

Rigorous statistical tests were performed to assess the significance of observed differences:

* **Core A/B Test (Ad Group vs. PSA Control):**
    * **Ad Group Conversion Rate:** $\approx 2.55\%$ (14,423 conversions out of 564,577 users)
    * **PSA Group Conversion Rate:** $\approx 1.79\%$ (420 conversions out of 23,524 users)
    * **Result:** A **Z-statistic of 7.3701** and a **p-value of 0.0000** (p < 0.0001) led to the rejection of the null hypothesis.
    * **Conclusion:** There is a **highly statistically significant difference**, confirming the ad campaign's success in driving conversions compared to the control.

* **Conversion Rate by Day of Week:**
    * **Monday** ($\approx 3.28\%$) and **Tuesday** ($\approx 2.98\%$) were generally the most effective days.
    * **Saturdays** ($\approx 2.11\%$) showed the lowest *overall* conversion rates, with a statistically significant difference compared to Mondays (p-value 0.0000).

* **Conversion Rate by Total Ads Seen:**
    * Users in the **lowest ads bin (0-2 ads)** had a very low conversion rate ($\approx 0.19\%$).
    * Users in the **highest ads bin (143-2065 ads)** showed a vastly superior conversion rate ($\approx 16.04\%$).
    * **Result:** This difference was highly statistically significant (p-value 0.0000), indicating that sufficient ad exposure is crucial for conversion.

### Phase 4: Granular Performance - Day-Hour Interaction

A detailed heatmap analysis of conversion rates by `Most Ads Day` and `Most Ads Hour` revealed critical insights into optimal timing:

* **Peak Conversion Hotspots:**
    * **Saturday 5:00-6:00 AM:** Surprisingly exhibited the **highest conversion rates (5.32% and 4.91%)**, highlighting a highly receptive niche audience during these early hours.
    * **Tuesday 4:00 PM (4.53%), Monday 2:00-3:00 PM (4.44%, 4.25%), and Sunday 8:00 PM (4.32%)** also stood out as strong conversion windows.
* **Consistent Trends:** Late afternoon/evening (2:00 PM - 10:00 PM) generally showed strong performance across most days.
* **Inefficient Hours:** Deep night hours (1:00 AM - 4:00 AM) consistently yielded very low conversion rates across almost all days, indicating these are inefficient times for ad exposure.
* **Note on Daily Averages vs. Hourly Peaks:** While Saturday's *overall* lower conversion rate (avg. $\approx 2.11\%$) masks specific high-performing early morning hours, Monday's consistent overall strength (avg. $\approx 3.28\%$) is further amplified by its significant mid-afternoon peaks. This emphasizes that optimal ad timing requires precise hour-by-hour analysis to identify both hidden opportunities and concentrated strengths within daily trends.

### Phase 5: Potential Revenue Estimation

An estimation of potential revenue was performed, based on an assumed average revenue per conversion:

* **Assumption:** Average Revenue per Conversion = **$75.00** (This is a placeholder and should be replaced with actual business data for precise results).
* **Baseline Revenue (PSA Group):** **$31,500.00**
* **Projected Revenue (Ad Strategy rolled out to all users in experiment):** **$1,126,796.80**
* **Estimated Incremental Revenue (Gain from Ad Strategy):** **$1,095,296.80**

This analysis projects over **$1.09 Million in additional revenue** from the ad campaign, given the stated revenue assumption.

## Key Recommendations

Based on these compelling findings, here are actionable recommendations for optimizing future marketing efforts:

1.  **Strategic Ad Scheduling & Precision Timing:**
    * **Capitalize on Niche Opportunities:** Invest specifically in the **Saturday 5:00-6:00 AM** window, as it demonstrates exceptionally high conversion.
    * **Reinforce Peak Periods:** Prioritize ad spend on **Monday/Tuesday afternoons (2:00-3:00 PM)** and **Sunday evenings (8:00 PM)**.
    * **Reduce Waste:** Significantly reduce or eliminate ad exposure during **deep night hours (1:00 AM - 4:00 AM)** due to extremely low conversion rates.

2.  **Optimize Ad Exposure Thresholds:**
    * Implement strategies (e.g., advanced retargeting, smart frequency capping) to ensure users receive a sufficient number of ad exposures (beyond just 1-2 ads), as higher total ad views strongly correlate with conversion.

3.  **Validate Financial Metrics:**
    * Collaborate with finance/product teams to obtain the precise average revenue per conversion. This will allow for highly accurate ROI and profitability analyses.

4.  **Continuous Performance Monitoring:**
    * Regularly track conversion rates, user behavior, and the effectiveness of time-based strategies to adapt to evolving market trends and user habits.

## Conclusion

This project successfully leveraged data analysis and A/B testing techniques to demonstrate the significant impact of the ad campaign on user conversions. By understanding the intricate relationships between ad exposure, timing, and user behavior, the derived recommendations provide a clear roadmap for maximizing marketing efficiency and driving substantial incremental revenue.

---.* **Day and Hour Trends:** Preliminary observations showed potential variations in conversion rates based on the day of the week and hour of the day.
* **Impact of Total Ads:** A clear trend emerged indicating higher conversion rates with increased ad exposure.

### Phase 3: Hypothesis Testing & A/B Testing

Rigorous statistical tests were performed to assess the significance of observed differences:

* **Core A/B Test (Ad Group vs. PSA Control):**
    * **Ad Group Conversion Rate:** $\approx 2.55\%$ (14,423 conversions out of 564,577 users)
    * **PSA Group Conversion Rate:** $\approx 1.79\%$ (420 conversions out of 23,524 users)
    * **Result:** A **Z-statistic of 7.3701** and a **p-value of 0.0000** (p < 0.0001) led to the rejection of the null hypothesis.
    * **Conclusion:** There is a **highly statistically significant difference**, confirming the ad campaign's success in driving conversions compared to the control.

* **Conversion Rate by Day of Week:**
    * **Monday** ($\approx 3.28\%$) and **Tuesday** ($\approx 2.98\%$) were generally the most effective days.
    * **Saturdays** ($\approx 2.11\%$) showed the lowest *overall* conversion rates, with a statistically significant difference compared to Mondays (p-value 0.0000).

* **Conversion Rate by Total Ads Seen:**
    * Users in the **lowest ads bin (0-2 ads)** had a very low conversion rate ($\approx 0.19\%$).
    * Users in the **highest ads bin (143-2065 ads)** showed a vastly superior conversion rate ($\approx 16.04\%$).
   * **Result:** This difference was highly statistically significant (p-value 0.0000), indicating that sufficient ad exposure is crucial for conversion.

### Phase 4: Granular Performance - Day-Hour Interaction

A detailed heatmap analysis of conversion rates by `Most Ads Day` and `Most Ads Hour` revealed critical insights into optimal timing:

* **Peak Conversion Hotspots:**
    * **Saturday 5:00-6:00 AM:** Surprisingly exhibited the **highest conversion rates (5.32% and 4.91%)**, highlighting a highly receptive niche audience during these early hours.
    * **Tuesday 4:00 PM (4.53%), Monday 2:00-3:00 PM (4.44%, 4.25%), and Sunday 8:00 PM (4.32%)** also stood out as strong conversion windows.
* **Consistent Trends:** Late afternoon/evening (2:00 PM - 10:00 PM) generally showed strong performance across most days.
* **Inefficient Hours:** Deep night hours (1:00 AM - 4:00 AM) consistently yielded very low conversion rates across almost all days, indicating these are inefficient times for ad exposure.
* **Note on Daily Averages vs. Hourly Peaks:** While Saturday's *overall* lower conversion rate (avg. $\approx 2.11\%$) masks specific high-performing early morning hours, Monday's consistent overall strength (avg. $\approx 3.28\%$) is further amplified by its significant mid-afternoon peaks. This emphasizes that optimal ad timing requires precise hour-by-hour analysis to identify both hidden opportunities and concentrated strengths within daily trends.

### Phase 5: Potential Revenue Estimation

An estimation of potential revenue was performed, based on an assumed average revenue per conversion:

* **Assumption:** Average Revenue per Conversion = **$75.00** (This is a placeholder and should be replaced with actual business data for precise results).
* **Baseline Revenue (PSA Group):** **$31,500.00**
* **Projected Revenue (Ad Strategy rolled out to all users in experiment):** **$1,126,796.80**
.
