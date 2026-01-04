# Leveraging Social Determinants of Health (SDOH) Analytics to Address Healthcare Disparities

🔗 **View Dashboard**  
*(Interactive Power BI dashboard showcasing health equity insights across regions and populations)*

---

## Table of Contents
- [Description](#description)
- [Business Introduction](#business-introduction)
- [Business Problem](#business-problem)
- [Aim](#aim)
- [Processes](#processes)
- [Dashboard Design](#dashboard-design)
- [Automation Workflow](#automation-workflow)
- [Key Insights](#key-insights)
- [Recommendations](#recommendations)

---

## Description
This project focuses on analysing **Social Determinants of Health (SDOH)** to understand how non-clinical factors such as education, transport access, housing stability, income, and health literacy influence health outcomes in underserved communities.

The analysis was carried out using **Excel, Power Query, Power BI, and Power Automate**, with the goal of building a centralized, automated analytics solution that supports **data-driven public health decision-making and health equity monitoring**.

---

## Business Introduction
HealthLink Analytics is a healthcare data organization committed to addressing health disparities through data-driven insights. The organization specialises in analysing Social Determinants of Health (SDOH) — socioeconomic and environmental factors that significantly impact population health outcomes.

By integrating clinical and social data, HealthLink supports public health agencies, healthcare providers, and policymakers in allocating resources more effectively, particularly within underserved communities.

---

## Business Problem

### Data Fragmentation
Demographic, clinical, and SDOH datasets exist across separate systems, preventing a unified view of population health risks.

### Manual Data Processing
Data collection and reporting relied heavily on manual workflows, leading to inefficiencies, delays, and increased risk of human error.

### Lack of Real-Time Insights
Dashboards required manual refresh, limiting the ability to respond quickly to emerging health trends and high-risk populations.

### Limited Geospatial Visibility
The absence of region-level insights restricted the ability to identify geographic disparities and target interventions effectively.

---

## Aim
The aim of this project was to develop a **centralized SDOH analytics platform** that enables real-time monitoring of health equity indicators and supports proactive, evidence-based public health interventions.

---

## Processes

### Data Preparation
The dataset included demographic data, geographic attributes, SDOH indicators, and health outcome measures.  
Initial data cleaning was performed in **Excel and Power Query**, including:
- Removing duplicates  
- Handling missing values  
- Standardising categorical fields (education, literacy, income, transport access)  
- Validating data consistency  

### Data Modelling & Calculations
The cleaned dataset was modelled in **Power BI**, with relationships created across demographics, geography, SDOH factors, and health outcomes.

Custom **DAX measures** were created to calculate:
- Total Population  
- Population at Risk (%)  
- Social Stability Index (%)  
- Preventive Care Rate (%)  
- Hospitalisation Rate (%)  
- Region-level risk rankings  

---

## Dashboard Design
The dashboard was designed with a strong emphasis on **visual storytelling and interpretability**:
- Colour coding to distinguish stable, moderate-risk, and high-risk populations  
- Conditional formatting to highlight critical regions and SDOH challenges  
- Dynamic slicers for region, education level, transport access, and health literacy  
- KPI cards to surface key population-level indicators  

These design choices allow stakeholders to quickly identify disparities and prioritise action.

---

## Automation Workflow
An automated data pipeline was implemented using **Power Automate**:

**Google Forms → Power Automate → Master Dataset → Power BI Auto-Refresh**

### Automated Steps
1. Capture form responses  
2. Map responses to dataset schema  
3. Append data to the master dataset  
4. Send confirmation email  
5. Trigger automatic Power BI dataset refresh  

This workflow eliminated manual data entry and ensured dashboards remain up to date.

---

## Key Insights
- Preventive care uptake was high, yet hospitalisation rates remained elevated  
- Low health literacy emerged as the most prevalent SDOH challenge  
- Certain regions consistently showed higher vulnerability and risk  
- Rural communities were disproportionately affected by transport and education barriers  

---

## Recommendations

### Insight-Driven
- Prioritise high-risk regions for targeted outreach and screening programmes  
- Strengthen health literacy initiatives using simple, community-led education  
- Improve transport access to reduce delays in care  
- Expand preventive care efforts for high-burden chronic diseases  

### Operational & Strategic
- Engage community leaders and NGOs to guide culturally appropriate interventions  
- Strengthen data governance through automated quality checks  
- Document workflows to support scalability and replication across regions  
- Provide mobile dashboard access for frontline health workers  

---

## Tools Used
- **Excel** – Data preparation  
- **Power Query** – Data cleaning and transformation  
- **Power BI** – Data modelling, DAX, and dashboard development  
- **Power Automate** – Workflow automation  
