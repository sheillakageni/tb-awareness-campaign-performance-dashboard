##TB Awareness Campaign Performance Dashboard

##Project Overview

This project analyzes the performance of a digital-first public health communication initiative: the Tuberculosis (TB) Awareness Digital Campaign executed on behalf of Amref Health Africa and the National TB Program (Ministry of Health, Kenya) as described in the companion documentation, "END OF SOCIAL MEDIA CAMPAIGN REPORT .docx".

Using Power BI, this interactive dashboard tracks metrics from "TB_Campaign_Portfolio_Dataset.xlsx" into strategic insights. It helps public health program managers and creative partners evaluate campaign performance across various social platforms, content formats, messaging themes, and target demographics to maximize resource efficiency and drive community health behavior change.

##Business Problem & Context

Public health communication involves complex logistics, cross-functional stakeholder coordination, and significant resource investments in creative assets.  Ministry of Health's Communications Section requires clear visibility into audience reach and engagement to justify creative production costs and guide future deployment strategies.

This dashboard directly solves that reporting gap by answering critical business questions:

Which platform maximized resources and reached most people?

How did unique audience exposure shift over the campaign period?

Which content formats optimized engagement?

Which public health themes resonated most deeply with the Public?

###Technical Architecture & Data Modeling

##Data Model Architecture

Below is the data model layout within Power BI, featuring the core data tables and calculated measures:

The tables are configured in a Star Schema with one-to-many. The unidirectional relationships point from the dimension tables (Campaign Themes, Content Types, Platforms) to the core fact table (Fact TB Campaign).

###Key DAX Measures

The calculations on the dashboard are driven by explicit DAX measures compiled inside the semantic model to maintain strict analytical control:

Total Reach = SUM('Fact TB Campaign'[Reach])


Total views = SUM('Fact TB Campaign'[Views])


Total engagement = SUM('Fact TB Campaign'[Likes]) + SUM('Fact TB Campaign'[Comments]) + SUM('Fact TB Campaign'[Shares])


Average Engagement Rate = AVERAGE('Fact TB_Campaign'[Engagement_Rate])


Earned Media Value = SUM('Fact TB_Campaign'[EMV_USD])


###Dashboard Preview

Executive Summary

As captured in "Tb Awareness- Dashboard screenshot.JPG", the primary report layout tracks high-level operational performance:

Filtered Dashboard Examples

Platform Performance Filter

TikTok Campaign – Youth Audience

KPIs & Portfolio Performance Metrics

The complete data portfolio yielded the following definitive campaign tracking results:

Total Reach: 512K unique users

Total Views: 489K  views

Total Engagement: 29K  interactions (likes, comments, and shares)

Average Engagement Rate: 6.08%

Total Earned Media Value (EMV): $262,153K

## Tools Used

Power BI Desktop: Core dashboard development, semantic modeling, and data visualization.

Power Query: Data extraction, transformation, and structural formatting.

DAX (Data Analysis Expressions)


### Dataset

This project utilizes a structured campaign dataset to show real-world digital health campaigns. The Fact table captures:

Platform: TikTok, X (Twitter), Facebook, Instagram

Content Type: Animation, Short Video, Quote Card, Image, Reel

Campaign Theme: TB Testing, Free Treatment, Stigma Reduction, TB Prevention, TB Symptoms, Treatment Adherence

Audience: Youth (20–35), Men 24–35, General Public, Key & Vulnerable Populations, Women

Performance Columns: Reach, Views, Likes, Comments, Shares, Engagement Rate, Earned Media Value (EMV)

### Key Insights & Operational Analysis

1. Platform Domination & ROI

TikTok was the leading platform, commanding 52.9% of total exposure with 270,973 unique users and $142.86K in EMV.

X (Twitter) came in second, driving 183,349 in reach and $89.94K in EMV.


2. Timeline  & Audience Exposure

Campaign reach fluctuated significantly throughout the execution period (June 9 to June 23), characterized by sharp peaks and valleys.

The campaign had its absolute performance peak on June 21st, followed by standard post-campaign stabilization.

3. Creative Efficiency & Production Value

Quote Cards generated the highest overall audience interaction, accounting for 27.71% of total engagement share.

Animations and Short Videos closely followed, securing 20.63% and 19.05% of the engagement share, respectively.

Operational Takeaway:  The data validates the project coordination strategy to negotiate a single, high-impact 124-second feature animation to maximize cross-platform deployment rather than overspending on multiple separate short assets.

4. Public Health Message Resonance

TB Testing emerged as the most resonant campaign theme, driving the highest total engagement. This confirms that direct, actionable, health-seeking calls to action dramatically outperform abstract concepts.

Free Treatment and Stigma Reduction themes also tracked strongly, indicating high community appetite for messaging that explicitly lowers institutional barriers to care.

### Skills Demonstrated

Data Preparation: Table separation and structural modeling using Power Query.

Power BI Development:  DAX measures, dynamic filtering, and dashboard design.

Strategic Business Storytelling: Translating media metrics into clear operational insights (ROI, production allocation, and audience targeting).

Professional Workflow: Git version control, repository layout management, and Markdown documentation.

### Repository Structure

├── data/
│   └── TB_Campaign_Portfolio_Dataset.xlsx    # Consolidated clean source data
├── images/
│   ├── TB AWARENESS SCREENSHOT-Dashboard.JPG  # Executive dashboard capture
│   ├── Tb awareness screenshot- X.JPG        # Platform deep-dive screenshot
│   ├── Tb awareness screenshot - Tiktok and Youth.JPG
│   └── polished relationship.JPG             # Power BI relationships and semantic model
├── pbix/
│   └── Tb_Awareness_Dashboard.pbix           # Power BI working file
└── README.md                                 # Project documentation


Created by Sheilla Kageni

Program & Project Management, Data Analytics & Operations Specialist
