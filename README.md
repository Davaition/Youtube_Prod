
# YouTube Regional Engagement Analysis

## Project Background

Ken Jee is a prominent content creator in the data science and analytics industry, known for sharing practical tutorials and career advice. His YouTube channel operates on an audience-engagement business model, where monetization is driven by views, watch time, and subscriber growth. This analysis was conducted from the perspective of a data analyst supporting the channel’s strategic decision-making.

The goal of this project was to answer the question:  
**“How do viewer engagement metrics vary across regions, and which regions are showing upward trends in engagement and subscriber growth over time?”**

Insights and recommendations are provided on the following key areas:

- **Regional Watch Time & Total Views** 
- **Subscriber Conversion & Engagement Rates** 
- **Monthly Subscriber Trends & Growth** 
- **Strategic Regional Opportunities** 


An interactive Power BI dashboard used to explore performance trends can be found here [youtube_analytics_project.pbix].

---

## Data Structure & Initial Checks

The company’s main database structure includes five core tables:

- `Country_Lookup`: Maps `country_id` to country and region (APAC, NA, EMEA, LATAM)
- `Calendar_Lookup`: Provides month, quarter, year mapping
- `Video_Stats`: Engagement metrics (watch time, likes, views, sub conversion)
- `Video_Lookup`: Basic metadata (video title, type, publish date)
- `Video_Trend`: Tracks trend metrics daily (impressions, conversions, watch%)

![ERD](Images/ERD.png)

---

## Executive Summary

An analysis of 2020-2022 YouTube videos Ken Jee’s channel revealed strong regional disparities in viewer behaviour and subscriber growth across APAC, EMEA, NA, and LATAM. APAC leads in total views and subscriber count, accounting for nearly 40% of total engagement, while NA shows the highest average watch time at over 4 minutes per session. LATAM, although contributing only 6% of total views, demonstrated the highest subscriber conversion rate at 30.5%, signalling untapped potential.

Performance peaks consistently during Q2—especially in May—suggesting an opportunity to synchronise campaigns around this period. Subscriber growth trends show early-year strength but taper off mid-year, highlighting the need for retention strategies and content refreshes. Localised content in LATAM and long-form, high-retention content in NA are strategic levers for driving further growth. These insights can guide content planning, regional targeting, and investment in personalization to maximize channel performance and audience retention.

### Key Findings

1. APAC leads in total views (1.8M) and subscribers, making it the most scalable region.
2. LATAM has the highest conversion rate (30.5%), signalling a highly engaged audience.
3. NA has the highest average watch time (4m 03s), making it ideal for monetisation strategies.

![Dashboard Overview](Images/Complete_Dashboard.png)

---

## Insights Deep Dive

### Section 1: Regional Watch Time & Total Views

- APAC peaks in May with 531K views; average watch time: 3m 05s
- EMEA maintains steady growth; watch time: 3m 36s
- NA has the deepest engagement with 4m 03s avg watch time
- LATAM lowest total views (0.3M) but worth investing in due to the high subscriber conversion rate

![Regional Engagement](Images/Regional_Stats.png)

---

### Section 2: Subscriber Conversion & Engagement Rates

- LATAM has the highest conversion rate: 67%
- Peak months for conversion: June - October
- All Regions display a steady decline in subscribers gained monthly throughout the year
- NA lags slightly despite strong engagement

![Conversion Trends](Images/Trend_Charts.png)

---

### Section 3: Monthly Subscriber Trends & Growth

- Highest subscriber gains in APAC and EMEA
- Strong growth in April and May, especially in APAC (5.75%)
- LATAM’s growth % is low, but conversion efficiency is high

![Growth Metrics](Images/Trend_Heatmaps.png)

---

### Section 4: Strategic Regional Opportunities

- LATAM shows the highest conversion rate but low view count, indicating strong audience potential if better targeted.
- NA has the longest average watch time, making it ideal for long-form content that benefits from strong retention.
- APAC leads in views and subscriber volume, making it the most effective region to pilot and scale new content.
- EMEA has stable metrics but diverse audiences, suggesting localisation is needed to boost relevance and engagement.

---

## Recommendations

For the Content Strategy Team:

- Translate/localise content for LATAM to increase viewership while maintaining high conversion
- Use NA as a hub for long-form educational videos
- Invest in Q2 campaigns, especially May when all regions peak
- Launch experimental content in APAC — scalable and growing
- Re-evaluate strategy for EMEA — consider subtitling and SEO targeting

---

## Assumptions and Caveats

- Some countries missing region tags were excluded or lumped into "Other"
- `is_outlier = TRUE` values were filtered out to reduce noise
- Monthly-level aggregations hide yearly spikes
- No time zone normalisation applied to posting dates
  
---

## Questions for Stakeholders Before Strategic Rollout

- Regional Mapping Consistency
  - Should the regional grouping (APAC, EMEA, NA, LATAM) follow YouTube’s internal schema, or be adjusted based on marketing segmentation?
  - How should countries without an assigned region be treated (e.g., "Other", unknown)?

- Watch Time Interpretation
  - Should watch time be assessed by average per video or total minutes watched per region when deciding content length strategies?
  - Is there a minimum engagement threshold that defines "high-performing" content?

- Subscriber Growth vs. Conversion
  - Should higher subscriber conversion rates (like in LATAM) be prioritised over higher subscriber volume (like APAC)?
  - How should we define success, absolute subscriber gain or percentage growth/conversion?

- Campaign Timing and Seasonality
  - Are there known marketing pushes (e.g., course launches, collabs) during months like May and October that could explain engagement spikes?
  - Should campaigns be uniformly launched across regions, or staggered to reflect historical performance trends?

- Localisation Strategy
  - What content localisation strategies (translation, subtitling, region-specific topics) can be used?
  - Is there an appetite to test region-specific playlists or region-led community engagement efforts?

---

