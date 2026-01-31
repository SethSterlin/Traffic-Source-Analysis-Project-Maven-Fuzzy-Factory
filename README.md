![enter image description here](https://github.com/SethSterlin/Sales-Trend-Analysis-Project-Maven-Fuzzy-Factory/blob/main/1728341011079.jpg)

# Sales Trend Analysis Project – Maven Fuzzy Factory

## Project Summary

This project focuses on **analyzing traffic sources and marketing performance** to understand  
**where customers come from and which channels drive the highest-quality traffic and conversions**.

By linking **website session data with order data**, I evaluated both **traffic volume and conversion efficiency** across marketing channels. The analysis supports **data-driven decisions on ad spend, bidding strategy, and campaign optimization**, with the ultimate goal of improving **marketing ROI and sustainable growth**.

Using SQL and visualization tools, I analyzed traffic sources, conversion rates, trends over time, and performance by device type to identify actionable insights for marketing strategy optimization.

---

## Project Highlights

- Identified **Google Search (nonbrand)** as the primary traffic source (>90% of sessions)  
- Measured **conversion rate below benchmark** (2.88% vs expected 4%)  
- Analyzed **traffic trends before and after bid adjustments**  
- Discovered significant **conversion rate differences by device type**  
- Demonstrated that **device-level bid optimization improved desktop traffic volume**  

---

## Dataset Used

[Maven Fuzzy Factory](https://github.com/SethSterlin/A-B-Landing-Page-Test-Maven-Fuzzy-Factory/blob/main/Calculate%20Bounce%20Rate.sql)  

---

## Objectives

1. Identify top traffic sources driving website sessions  
2. Evaluate conversion efficiency by marketing channel  
3. Assess the impact of bid changes on traffic volume over time  
4. Compare conversion rates by device type to optimize bidding strategy  
5. Provide data-backed recommendations to improve marketing ROI  

---

## Key Metrics & Analysis

### Key Metrics
- Sessions  
- Orders  
- Conversion Rate (CVR)  
- Traffic Source Distribution  
- Sessions by Device Type  
- Weekly Traffic Trends  

### Key Analyses
- Traffic source analysis to identify top acquisition channels  
- Session-to-order conversion rate calculation  
- Trend analysis of traffic volume over time  
- Pre- and post-bid change comparison  
- Device-level conversion rate analysis (Desktop vs Mobile)  

### Key Findings
- **Google Search (nonbrand) CVR:** 2.88% (below 4% benchmark)  
- **Desktop CVR:** 3.73%  
- **Mobile CVR:** 0.96%  
- Traffic volume dropped ~65% after peak, influenced by bid changes and other factors  
- Increasing desktop bids successfully restored desktop traffic volume  

---

## Business Outcomes

- Identified underperforming traffic sources requiring bid optimization  
- Reduced inefficient ad spend on low-converting segments  
- Improved budget allocation through **device-level bidding strategy**  
- Enabled more accurate evaluation of marketing campaign effectiveness  
- Provided actionable insights to improve **conversion efficiency and ROI**  

---

## Tools Used

- **SQL** — Traffic source analysis, conversion rate calculation, trend analysis  
- **Tableau** — Traffic trends and campaign performance visualization  
- **GitHub** — Version control and project documentation  
- **Relational Database** — Website sessions, pageviews, and order data  

---

## Sales & Traffic Source Analysis – From Acquisition to Conversion

Understanding where customers come from and which marketing channels drive the highest quality traffic is a fundamental business concept. **Traffic source analysis** helps me identify the origins of website visitors—whether through **email, social media, search engines, direct visits, or paid** campaigns—and evaluate how well each channel converts visitors into customers.

This analysis not only measures visitor volume but also conversion rates, which represent the percentage of sessions that lead to sales or revenue-generating actions. By linking website session data with order data, I can assess the effectiveness of marketing campaigns, optimize ad spend, and improve overall return on investment.

In this project, I explored three key datasets: website sessions, pageviews, and orders, examining how they interact to provide insights into user behavior and campaign performance. With this foundation, I **used SQL queries and visualization tools to analyze traffic sources and conversion efficiency**, enabling data-driven marketing decisions.

## STEP 1 : Finding Top Traffic Source

In this step, I analyzed web session data from the early launch phase of an e-commerce startup to help the marketing team answer a key business question:

> **“Where are our website visitors coming from, and which channels are driving the most traffic?”**

![enter image description here](https://github.com/SethSterlin/Sales-Trend-Analysis-Project-Maven-Fuzzy-Factory/blob/main/screenshot20250706134243.png?raw=true)

### Based on my findings

-   **Google Search (nonbrand)** accounted for the largest share of traffic, indicating successful customer acquisition efforts.
    
-   **Brand campaigns** drove significantly fewer sessions, suggesting a need to increase brand awareness.
    

## STEP 2: Calculate Conversion Rate for Google Search (nonbrand) Campaign

After identifying _Google Search (nonbrand)_ as the primary traffic source contributing over 90% of total sessions, I focused on evaluating its conversion efficiency.

Given the large volume of traffic, small improvements in conversion rate (CVR) could greatly increase revenue.

🎯 **Business Question:**

> Is the Google Search (nonbrand) campaign not only driving traffic but also converting visitors effectively?

I set a performance benchmark:

> **Expected CVR ≥ 4%**

By analyzing session-to-order conversion, I aimed to validate whether this campaign attracted quality leads or primarily high-volume, low-intent visitors.

This analysis connects traffic data with sales outcomes, enabling me and the decision-makers to evaluate if the current marketing spend is justified or requires adjustment.

![Conversion Rate Chart](https://github.com/SethSterlin/Sales-Trend-Analysis-Project-Maven-Fuzzy-Factory/blob/main/screenshot20250706140547.png?raw=true)

**I found the conversion rate (CVR) for the "Google Search (nonbrand) " campaign was 2.88%, which is below the expected benchmark of 4%.**

Given the lower-than-expected conversion rate, the immediate next step is to **adjust bidding strategies to reduce ad spend on underperforming traffic sources**. This will help control acquisition costs while maintaining quality traffic.

<p align="center">
  <img src="https://github.com/SethSterlin/Sales-Trend-Analysis-Project-Maven-Fuzzy-Factory/blob/main/screenshot20250711184933.png?raw=true" />
</p>

Simultaneously, I plan to **analyze performance trends across different device types** to identify where conversion efficiencies vary, allowing me to **refine targeting and bidding strategies accordingly**.

By continuously monitoring these metrics and iterating on campaign elements such as the landing page and ad creatives, I aim to improve conversion rates, optimize marketing ROI, and support sustainable growth.

## STEP 3: Analyze Traffic Source Trending Over Time
Based on the conversion rate (CVR) analysis, **the marketing team decided to bid down on Google Search (non-brand) on May 15, 2012** campaigns.

I would like to further explore whether this bid change could have been a contributing factor to the observed **drop in traffic volume**.

To understand how the _Google Search (nonbrand)_ campaign's traffic volume changed during the initial launch period, I analyzed weekly session counts.

Using session data grouped by week, I observed the following trend:  
![enter image description here](https://github.com/SethSterlin/Sales-Trend-Analysis-Project-Maven-Fuzzy-Factory/blob/main/Traffic%20Source%20Trending.png?raw=true)


From this, I observe:

-   📈 A **peak** in traffic during the week of **2012-04-01** (1,152 sessions).
    
-   📉 A **sharp and consistent drop** in traffic starting from **2012-04-08**, falling to **399** by **2012-05-06**.
    
-   This represents a **65% drop** from the peak.

> Although there was a clear drop in sessions following the bid reduction on April 15, 2012, there were already signs of declining traffic volume in the weeks prior. This indicates that the traffic volume may have been influenced by multiple factors beyond just the bid change.
  

## STEP 4: Conversion Rate by Device Type and Bid Optimization

Since I was found Google Search (nonbrand) traffic volume is sensitive to bid changes, I analyzed conversion rates by device type. This helps me adjust bids separately for desktop and mobile, improving ad spend efficiency and maximizing campaign performance.

![enter image description here](https://github.com/SethSterlin/Sales-Trend-Analysis-Project-Maven-Fuzzy-Factory/blob/main/screenshot20250706145453.png?raw=true)

I discovered that the conversion rate for desktop users (3.73%) is significantly higher than for mobile users (0.96%) in the Google Search (nonbrand) campaign. This indicates that bidding the same across devices is inefficient.

To optimize ad spend and improve campaign performance, bids should be adjusted by device type — reducing bids on low-converting mobile traffic and prioritizing desktop traffic.

This device-level analysis helps maximize return on investment and guides smarter bidding strategies.

## STEP 5: Traffic Source Segment Trending by Device Type

Based on the previous analysis, the marketing team increased bids for the _Google Search (nonbrand)_ campaign targeting desktop users on May 19, 2012. This adjustment aimed to regain volume and improve efficiency for desktop traffic specifically.

In this step, I analyzed weekly session trends for desktop and mobile traffic from April 15th onwards to observe the impact of the bid increase.

![enter image description here](https://github.com/SethSterlin/Sales-Trend-Analysis-Project-Maven-Fuzzy-Factory/blob/main/Traffic%20Source%20Segment%20Trending%20by%20Device%20Type.png?raw=true)

---

### Key Insights

-    **Desktop CVR: 3.73%**

-    **Mobile CVR: 0.96%**

After increasing bids for desktop traffic starting the week of May 20, 2012, desktop sessions showed a significant increase, rising from around 400 sessions per week to over 660 sessions. Meanwhile, mobile sessions continued to decline slightly.

This confirms that device-level bid adjustments can effectively boost traffic volume in targeted segments. It highlights the value of segmenting marketing efforts by device type to maximize campaign performance and optimize ad spend.

---

### Recommendation

-    Decrease bids for low-performing mobile traffic

-    Prioritize desktop traffic where conversion efficiency is significantly higher

-    This device-level analysis enables more precise budget allocation and improved ROI.

---

## Resources

- SQL Scripts:  
  [Sales Trend Analysis Project – Maven Fuzzy Factory SQL file](https://github.com/SethSterlin/Sales-Trend-Analysis-Project-Maven-Fuzzy-Factory/blob/main/Sales%20Trend%20Analysis%20Project%20%20%E2%80%93%20Maven%20Fuzzy%20Factory.sql)

- Tableau Dashboards:  
  [Traffic Source Trending Chart](https://public.tableau.com/views/TrafficSourceTrending_17517955194920/Sheet1?:language=th-TH&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)  
  [Traffic Source Segment Trending by Device Type](https://public.tableau.com/views/TrafficSourceSegmentTrendingbyDeviceType/Sheet1?:language=th-TH&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
