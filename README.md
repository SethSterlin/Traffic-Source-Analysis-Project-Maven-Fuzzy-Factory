![enter image description here](https://github.com/SethSterlin/Sales-Trend-Analysis-Project-Maven-Fuzzy-Factory/blob/main/1728341011079.jpg)

# Sales Trend Analysis Project – Maven Fuzzy Factory

## Project Background

In the early stage of an e-commerce business, marketing teams often face a critical challenge:  
**driving traffic efficiently while ensuring that visitors actually convert into customers.**  
With limited budgets and high competition in digital advertising, understanding *where traffic comes from*, *how users behave*, and *which channels truly drive revenue* becomes essential for sustainable growth.

This project uses the **Maven Fuzzy Factory** dataset, a realistic e-commerce database that captures the full customer journey — from website sessions and pageviews to orders, products, and refunds. The dataset reflects real-world business complexity, including multiple traffic sources, device types, and changing marketing strategies over time.

The primary business problem addressed in this analysis is:

**Are our marketing campaigns attracting high-quality traffic that converts, or are we paying for volume without sufficient return?**

To answer this, the project focuses on **traffic source analysis and conversion rate optimization**, two core pillars of performance marketing. By linking session-level data with order outcomes, the analysis evaluates not only *how much traffic* each channel generates, but also *how valuable that traffic is* in terms of actual sales.

Throughout the project, I simulate real decision-making scenarios faced by a marketing team — such as adjusting bids, reallocating budget across devices, and responding to declining performance. Using SQL and data visualization, the analysis translates raw data into actionable business insights that support smarter bidding strategies, improved ROI, and more efficient growth.

This project demonstrates how data can be used not just to report metrics, but to **guide strategic marketing decisions in a competitive e-commerce environment**.

### Project Highlights

- Identified **Google Search (nonbrand)** as the primary traffic source (>90% of sessions)  
- Measured **conversion rate below benchmark** (2.88% vs expected 4%)  
- Analyzed **traffic trends before and after bid adjustments**  
- Discovered significant **conversion rate differences by device type**  
- Demonstrated that **device-level bid optimization improved desktop traffic volume**

### Tools: `SQL` `MySQL` `Tableau`

---

## Data Structure and Key Concepts
### Dataset used

[Maven Fuzzy Factory](https://github.com/SethSterlin/A-B-Landing-Page-Test-Maven-Fuzzy-Factory/blob/main/Calculate%20Bounce%20Rate.sql)  

This ERD consists of six tables: `website_sessions`, `website_pageviews`, `orders, order_items`, products, and `order_item_refunds`, representing the full e-commerce funnel from traffic to refunds.
The dataset contains a total of 472,871 records across all tables.

![ERD Schema](https://github.com/SethSterlin/A-B-Landing-Page-Test-Maven-Fuzzy-Factory/blob/main/Maven%20ERD.png?raw=true)

Prior to beginning the analysis, a variety of quality control checks were performed to become familiar with the dataset. SQL was used during this stage to validate data integrity, identify missing or inconsistent values, and quickly explore large tables through aggregation and filtering.

### Understanding UTM Parameters (Traffic Source Tracking)

![enter image description here](https://github.com/SethSterlin/Sales-Trend-Analysis-Project-Maven-Fuzzy-Factory/blob/main/utm%20source.png)

This diagram illustrates how **UTM parameters** embedded in a URL are used to track the origin of website traffic and store it in a structured database format for analysis.

When a user visits the website through a URL. The UTM parameters provide critical marketing context:

- **utm_source** identifies the traffic source (e.g., Google Search, Bing Search).
- **utm_campaign** identifies the campaign type (e.g., brand, nonbrand).

These parameters are captured at the session level and stored in database columns such as `utm_source` and `utm_campaign`.  
As shown in the table, each website session can be classified based on its acquisition channel, enabling clear separation between paid search, branded traffic, and other channels.

This tracking mechanism is fundamental for **traffic source analysis**, as it allows analysts to:
- Attribute sessions and orders to specific marketing campaigns
- Measure conversion rates by channel and campaign
- Optimize bidding strategies and marketing spend based on performance

By linking UTM-tagged sessions with downstream order data, businesses can make data-driven decisions to improve marketing efficiency and ROI.

---

## Analysis Methodology

Understanding where customers come from and which marketing channels drive the highest quality traffic is a fundamental business concept. **Traffic source analysis** helps me identify the origins of website visitors—whether through **email, social media, search engines, direct visits, or paid** campaigns—and evaluate how well each channel converts visitors into customers.

This analysis not only measures visitor volume but also conversion rates, which represent the percentage of sessions that lead to sales or revenue-generating actions. By linking website session data with order data, I can assess the effectiveness of marketing campaigns, optimize ad spend, and improve overall return on investment.

In this project, I explored three key datasets: website sessions, pageviews, and orders, examining how they interact to provide insights into user behavior and campaign performance. With this foundation, I **used SQL queries and visualization tools to analyze traffic sources and conversion efficiency**, enabling data-driven marketing decisions.

### STEP 1 : Finding Top Traffic Source

In this step, I analyzed web session data from the early launch phase of an e-commerce startup to help the marketing team answer a key business question:

> **“Where are our website visitors coming from, and which channels are driving the most traffic?”**

![enter image description here](https://github.com/SethSterlin/Sales-Trend-Analysis-Project-Maven-Fuzzy-Factory/blob/main/screenshot20250706134243.png?raw=true)

**Based on my findings**

-   **Google Search (nonbrand)** accounted for the largest share of traffic, indicating successful customer acquisition efforts.
    
-   **Brand campaigns** drove significantly fewer sessions, suggesting a need to increase brand awareness.
    

### STEP 2: Calculate Conversion Rate for Google Search (nonbrand) Campaign

After identifying _Google Search (nonbrand)_ as the primary traffic source contributing over 90% of total sessions, I focused on evaluating its conversion efficiency.

Given the large volume of traffic, small improvements in conversion rate (CVR) could greatly increase revenue.

**Business Question:**

> Is the Google Search (nonbrand) campaign not only driving traffic but also converting visitors effectively?

I set a performance benchmark:

**Expected CVR ≥ 4%**

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

### STEP 3: Analyze Traffic Source Trending Over Time
Based on the conversion rate (CVR) analysis, **the marketing team decided to bid down on Google Search (non-brand) on May 15, 2012** campaigns.

I would like to further explore whether this bid change could have been a contributing factor to the observed **drop in traffic volume**.

To understand how the _Google Search (nonbrand)_ campaign's traffic volume changed during the initial launch period, I analyzed weekly session counts.

Using session data grouped by week, I observed the following trend:  
![enter image description here](https://github.com/SethSterlin/Sales-Trend-Analysis-Project-Maven-Fuzzy-Factory/blob/main/Traffic%20Source%20Trending.png?raw=true)


From this, I observe:

-   A **peak** in traffic during the week of **2012-04-01** (1,152 sessions).
    
-   A **sharp and consistent drop** in traffic starting from **2012-04-08**, falling to **399** by **2012-05-06**.
    
-   This represents a **65% drop** from the peak.

Although there was a clear drop in sessions following the bid reduction on April 15, 2012, there were already signs of declining traffic volume in the weeks prior. This indicates that the traffic volume may have been influenced by multiple factors beyond just the bid change.
  

### STEP 4: Conversion Rate by Device Type and Bid Optimization

Since I was found Google Search (nonbrand) traffic volume is sensitive to bid changes, I analyzed conversion rates by device type. This helps me adjust bids separately for desktop and mobile, improving ad spend efficiency and maximizing campaign performance.

![enter image description here](https://github.com/SethSterlin/Sales-Trend-Analysis-Project-Maven-Fuzzy-Factory/blob/main/screenshot20250706145453.png?raw=true)

I discovered that the conversion rate for desktop users (3.73%) is significantly higher than for mobile users (0.96%) in the Google Search (nonbrand) campaign. This indicates that bidding the same across devices is inefficient.

To optimize ad spend and improve campaign performance, bids should be adjusted by device type — reducing bids on low-converting mobile traffic and prioritizing desktop traffic.

This device-level analysis helps maximize return on investment and guides smarter bidding strategies.

### STEP 5: Traffic Source Segment Trending by Device Type

Based on the previous analysis, the marketing team increased bids for the _Google Search (nonbrand)_ campaign targeting desktop users on May 19, 2012. This adjustment aimed to regain volume and improve efficiency for desktop traffic specifically.

In this step, I analyzed weekly session trends for desktop and mobile traffic from April 15th onwards to observe the impact of the bid increase.

![enter image description here](https://github.com/SethSterlin/Sales-Trend-Analysis-Project-Maven-Fuzzy-Factory/blob/main/Traffic%20Source%20Segment%20Trending%20by%20Device%20Type.png?raw=true)

---

## Business Insights

This analysis reveals how **traffic quality, bidding strategy, and device-level behavior** directly impact conversion efficiency and marketing ROI in an e-commerce funnel.

### 1. Traffic Volume ≠ Traffic Quality

Although **Google Search (nonbrand)** contributed over **90% of total sessions**, its conversion rate was only **2.88%**, falling below the expected benchmark of **4%**.

**Insight:**  
High traffic volume alone does not guarantee revenue. Without sufficient purchase intent, aggressive acquisition can inflate costs while diluting efficiency.

**Business Implication:**  
Marketing success should be measured by **conversion-adjusted traffic**, not raw session counts.

### 2. Bid Reduction Was Not the Sole Cause of Traffic Decline

Weekly trend analysis showed that traffic volume had already begun declining **before** the bid reduction on April 15, 2012.  
After the peak on April 1, sessions dropped by **65%** within five weeks.

**Insight:**  
The bid change likely accelerated the decline, but underlying demand saturation or creative fatigue may have also played a role.

**Business Implication:**  
Bid adjustments should be supported by **trend diagnostics**, not treated as the single explanatory factor.

### 3. Device Behavior Is a Critical Optimization Lever

Conversion rates differed sharply by device type:

- **Desktop CVR:** 3.73%  
- **Mobile CVR:** 0.96%

**Insight:**  
Mobile traffic underperformed significantly, suggesting lower purchase intent or a suboptimal mobile experience.

**Business Implication:**  
Uniform bidding across devices is inefficient. **Device-level bid segmentation** is essential for cost control and performance optimization.

### 4. Smart Bidding Can Recover High-Quality Traffic

After increasing bids specifically for **desktop users** on May 19, 2012, desktop session trends stabilized while maintaining higher conversion efficiency.

**Insight:**  
Selective bid increases on high-performing segments can recover volume **without sacrificing ROI**.

**Business Implication:**  
Granular targeting enables growth without reverting to broad, inefficient spending.

### 5. Executive Takeaway

- Not all traffic is equally valuable  
- Conversion rate is a stronger decision metric than volume  
- Device-level segmentation materially improves marketing efficiency  
- Data-driven bid adjustments outperform blanket budget changes  

**Bottom line:**  
Sustainable growth comes from **optimizing traffic quality, not maximizing traffic quantity**.

---

## Recommendations

- Shift focus from traffic volume to traffic quality by prioritizing high-intent keywords and conversion-driven metrics over raw session counts  
- Implement device-level bidding strategies, increasing bids for high-performing desktop traffic while reducing exposure to low-converting mobile traffic  
- Investigate mobile funnel friction (UX, page speed, checkout drop-offs) before scaling mobile ad spend  
- Support bid adjustments with historical trend analysis to avoid reactive decisions based on short-term fluctuations  
- Establish a continuous optimization loop using regular performance reviews, controlled bid tests, and data-driven experimentation

---

## Resources

- SQL Scripts:  
  [Sales Trend Analysis Project – Maven Fuzzy Factory SQL file](https://github.com/SethSterlin/Sales-Trend-Analysis-Project-Maven-Fuzzy-Factory/blob/main/Sales%20Trend%20Analysis%20Project%20%20%E2%80%93%20Maven%20Fuzzy%20Factory.sql)

- Tableau Dashboards:  
  [Traffic Source Trending Chart](https://public.tableau.com/views/TrafficSourceTrending_17517955194920/Sheet1?:language=th-TH&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)  
  [Traffic Source Segment Trending by Device Type](https://public.tableau.com/views/TrafficSourceSegmentTrendingbyDeviceType/Sheet1?:language=th-TH&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
