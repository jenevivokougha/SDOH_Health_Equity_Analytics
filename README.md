# Leveraging Social Determinants of Health (SDOH) Analytics to Address Healthcare Disparities

*(Power BI dashboard showcasing health equity insights across regions and populations)*

<img width="1034" height="805" alt="Screenshot 2026-01-04 111523" src="https://github.com/user-attachments/assets/58b0e294-f69b-4988-a863-fe16e536d7b6" />

---

## Table of Contents
- [Description](#description)
- [Business Introduction](#business-introduction)
- [Business Problem](#business-problem)
- [Aim](#aim)
- [Processes](#processes)
- [Data Modelling & DAX](#data-modelling--dax)
- [Dashboard Design](#dashboard-design)
- [Automation Workflow](#automation-workflow)
- [Key Insights](#key-insights)
- [Recommendations](#recommendations)
- [Tools Used](#tools-used)

---

## Description
This project analyses **Social Determinants of Health (SDOH)** to understand how non-clinical factors such as education, transport access, housing stability, income, and health literacy influence health outcomes in underserved communities.

The solution was built using **Excel, Power Query, Power BI, and Power Automate**, delivering a centralized and automated analytics platform to support **data-driven public health decision-making and health equity monitoring**.

---

## Business Introduction
HealthLink Analytics is a healthcare data organization focused on addressing health disparities through actionable insights. The organisation specialises in analysing Social Determinants of Health (SDOH) — socioeconomic and environmental factors that significantly impact population health outcomes.

By integrating clinical and social data, HealthLink supports public health agencies, healthcare providers, and policymakers in allocating resources more effectively, particularly within underserved communities.

---

## Business Problem

### Data Fragmentation
Demographic, clinical, and SDOH datasets existed across separate systems, preventing a unified view of population-level health risks.

### Manual Data Processing
Data preparation and reporting relied heavily on manual workflows, increasing inefficiencies, delays, and the risk of human error.

### Lack of Real-Time Insights
Dashboards required manual refresh, limiting timely identification of emerging health trends and high-risk populations.

### Limited Geospatial Visibility
The absence of region-level analytics restricted the ability to identify geographic disparities and target interventions effectively.

---

## Aim
The aim of this project was to develop a **centralized SDOH analytics platform** that enables real-time monitoring of health equity indicators and supports proactive, evidence-based public health interventions.

---

## Processes

### Data Preparation
The dataset included demographic data, geographic attributes, SDOH indicators, and health outcome measures.  
Data cleaning and transformation were performed using **Excel and Power Query**, including:
- Removing duplicates  
- Handling missing values  
- Standardising categorical fields (education, literacy, income, transport access)  
- Validating data consistency  
- Merging datasets using **Left Outer Join** into a single consolidated table  

---

## Data Modelling & DAX
A structured data model was built in **Power BI**, linking demographics, geography, SDOH indicators, and health outcomes.

Custom **DAX measures** were created to support population segmentation, risk assessment, and performance monitoring.

### Example DAX Measures (Power BI)

```DAX
-- Total Population
Total Population =
COUNTROWS('Health_Data')

-- Preventive Care Rate (%)
Preventive Care Rate (%) =
DIVIDE(
    SUM('Health_Data'[Preventive_Care_Visits]),
    COUNTROWS('Health_Data')
)

-- Population at Risk (%)
Population at Risk (%) =
DIVIDE(
    CALCULATE(
        COUNTROWS('Health_Data'),
        'Health_Data'[Risk_Category] = "High Risk"
    ),
    COUNTROWS('Health_Data')
)

-- Social Stability Index (%)
Social Stability Index (%) =
DIVIDE(
    CALCULATE(
        COUNTROWS('Health_Data'),
        'Health_Data'[Risk_Category] = "Stable"
    ),
    COUNTROWS('Health_Data')
)


-- Hospitalisation Rate (%)
Hospitalisation Rate (%) =
DIVIDE(
    SUM('Health_Data'[Hospital_Admissions]),
    COUNTROWS('Health_Data')
)
```

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
