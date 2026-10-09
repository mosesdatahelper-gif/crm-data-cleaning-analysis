# CRM Data Cleaning & Sales Performance Analysis

## Project Overview

This project demonstrates a complete CRM data cleaning, validation, exploratory analysis, and business insight workflow using Python and Pandas.

The objective was to transform a raw CRM dataset into a clean, analysis-ready dataset and use the cleaned data to evaluate lead performance, sales pipeline activity, deal values, lead sources, industries, and countries.

The project simulates a real-world business analytics workflow where data quality must be addressed before reliable business decisions can be made.

---

## Business Objective

The primary objective was to clean and validate CRM data and generate actionable insights that could help a business improve its sales pipeline and conversion performance.

### Business Questions

1. How large is the sales pipeline?
2. What is the distribution of leads across different sales stages?
3. What is the overall closed-opportunity win rate?
4. Which lead sources generate the strongest performance?
5. Which industries have the highest deal values and win rates?
6. Which countries generate the strongest sales opportunities?
7. Does deal size meaningfully differentiate Won and Lost opportunities?
8. Where should the business focus its sales and marketing efforts?

---

## Dataset

The raw CRM dataset contains:

- **600 unique customer records**
- **12 columns**

### Columns

- Customer_ID
- Customer_Name
- Email
- Phone
- Company
- Industry
- Country
- Lead_Source
- Lead_Status
- Deal_Value
- Signup_Date
- Last_Contact_Date

---

## Data Cleaning & Preparation

The raw CRM dataset was cleaned and validated using **Python and Pandas**.

### Cleaning Activities

- Removed duplicate Customer IDs
- Standardized text fields
- Standardized customer names and categorical values
- Converted emails to lowercase
- Validated email formats
- Identified missing and unusable phone numbers
- Standardized missing values
- Converted date fields to proper datetime format
- Identified negative deal values
- Corrected negative deal values to zero
- Validated final data types
- Performed final duplicate and missing-value checks

### Final Data Quality

After cleaning:

- **600 unique CRM records**
- **0 duplicate Customer IDs**
- **30 missing/invalid email values**
- **46 missing/unusable phone values**
- Company, Industry, Country, and Lead Source fields contained no remaining missing values
- Date fields were converted to datetime format

The cleaned dataset was saved as:

`crm_data_cleaned.csv`

---

## Key Performance Indicators

| KPI | Result |
|---|---:|
| Total CRM Records | 600 |
| Total Associated Deal Value | ₦167.125M |
| Won Opportunities | 105 |
| Lost Opportunities | 107 |
| Won Deal Value | ₦29.30M |
| Lost Deal Value | ₦29.75M |
| Closed Opportunities | 212 |
| Closed Win Rate | 49.53% |
| Maximum Deal Value | ₦1M |
| Customers with ₦1M Deals | 58 |

> Note: Deal Value represents the associated/potential value of CRM opportunities rather than recognized revenue.

---

## Sales Funnel Analysis

The CRM pipeline contains six lead statuses:

| Lead Status | Leads | Share |
|---|---:|---:|
| New | 112 | 18.67% |
| Lost | 107 | 17.83% |
| Won | 105 | 17.50% |
| Qualified | 104 | 17.33% |
| Proposal | 91 | 15.17% |
| Contacted | 81 | 13.50% |

There were **212 closed opportunities**, consisting of:

- 105 Won
- 107 Lost

This produces an overall closed-opportunity win rate of **49.53%**.

Lost opportunities slightly exceeded Won opportunities, indicating an opportunity to improve conversion throughout the sales funnel.

---

## Lead Source Performance

Lead source performance revealed meaningful differences across acquisition channels.

### Key Findings

- **Referral** generated the highest total associated deal value at **₦34.70M**.
- Referral also produced the highest average deal value at approximately **₦318K**.
- **LinkedIn** produced the highest win rate among the established lead sources at **25.27%**.
- LinkedIn generated **23 Won opportunities**, the highest Won count among the established sources.
- Website generated **₦29.325M** in associated deal value but had the lowest established-source win rate at **10.68%**.
- The Unknown source had a 30% win rate, but its sample size was only 10 leads and therefore should not be treated as the strongest channel.

### Business Implication

Referral appears to be the strongest overall source for deal value, while LinkedIn shows strong conversion efficiency.

The business should strengthen referral programs and evaluate additional investment in LinkedIn while reviewing the performance of Website-generated leads.

---

## Industry Performance

### Key Findings

- **Manufacturing** generated the highest average deal value at approximately **₦328K**.
- **Technology** produced the highest industry win rate at **22.37%**.
- Technology also generated the highest Won deal value at **₦6.55M**.
- **Logistics** recorded a 20.00% win rate.
- Manufacturing had the lowest industry win rate at **13.41%**, despite having the highest average deal value.

### Business Implication

Technology represents a particularly attractive industry because it combines strong conversion performance with high Won deal value.

Manufacturing generates large opportunities, but its relatively low win rate suggests a need to investigate qualification, pricing, sales approach, or customer-fit issues.

---

## Country Performance

### Key Findings

- **United Kingdom** generated the highest total associated deal value at **₦35.125M**.
- **United States** generated the highest country win rate at approximately **19.83%**.
- United Kingdom followed closely at approximately **19.82%**.
- South Africa recorded an approximately **18.81%** win rate.
- Nigeria had the lowest country win rate at approximately **11.11%**.

### Business Implication

The United Kingdom and United States markets demonstrate strong commercial potential based on both deal value and conversion performance.

The relatively lower Nigerian win rate warrants further investigation into lead quality, customer segments, pricing, or sales processes.

---

## Deal Size Analysis

The analysis found that deal size alone does not strongly differentiate Won and Lost opportunities.

### Key Findings

- **58 customers** had the maximum deal value of ₦1M.
- These 58 records represented approximately **9.67% of all records**.
- Their combined deal value was **₦58M**, representing approximately **34.7% of total associated deal value**.
- Only **11 of the 58 ₦1M opportunities were Won**.
- This represents a win rate of approximately **18.97%** for these maximum-value opportunities.
- Average Won deal value was approximately **₦279K**.
- Average Lost deal value was approximately **₦278K**.

The small difference between average Won and Lost deal values indicates that deal size by itself is a weak predictor of sales outcome in this dataset.

---

## Key Business Findings

### 1. Referral is a high-value acquisition channel

Referral generated the highest total associated deal value and the highest average deal value.

### 2. LinkedIn demonstrates strong conversion efficiency

LinkedIn recorded the highest win rate among the established lead sources and the highest Won count.

### 3. Technology is a strong target industry

Technology produced both the highest industry win rate and the highest Won deal value.

### 4. The UK is the largest market by associated deal value

The United Kingdom generated the highest total associated deal value.

### 5. Deal size alone does not explain sales outcomes

Won and Lost opportunities had almost identical average deal values.

### 6. The sales funnel requires conversion improvement

Lost opportunities slightly exceeded Won opportunities among closed opportunities, indicating room to improve sales conversion.

---

## Business Recommendations

### 1. Strengthen Referral Acquisition

Develop a structured referral strategy because referrals generate strong deal value and conversion performance.

### 2. Invest in LinkedIn

LinkedIn demonstrates strong conversion efficiency and should be evaluated for increased targeted prospecting and lead generation.

### 3. Review Website Lead Performance

Website leads generate substantial deal value but have a relatively low win rate. Investigate lead quality, qualification, messaging, and conversion processes.

### 4. Prioritize Technology Opportunities

Technology combines strong win-rate performance with high Won deal value and should receive focused sales attention.

### 5. Investigate Manufacturing Conversion

Manufacturing produces high-value opportunities but has a relatively low win rate. The sales process for this segment should be examined.

### 6. Improve Closed-Opportunity Conversion

Because Lost opportunities slightly exceed Won opportunities, the business should analyze why qualified and proposal-stage opportunities are being lost.

### 7. Do Not Rely on Deal Size Alone

Sales prioritization should incorporate factors such as lead source, industry, country, engagement, and lead status rather than relying only on Deal Value.

---

## Tools & Technologies

- Python
- Pandas
- Jupyter Notebook
- Excel
- Data Cleaning
- Data Validation
- Exploratory Data Analysis
- CRM Analytics
- Sales Performance Analysis
- Business Intelligence
- Business Insight Generation

---

## Project Structure

```text
03_CRM_Data_Cleaning
│
├── README.md
│
├── 01_Case_Study
│   └── CRM_Data_Cleaning_Analysis_Case_Study.docx
│
├── 02_Data
│   ├── Project_3_CRM_Data_Cleaning_Raw.xlsx
│   └── crm_data_cleaned.csv
│
├── 03_Code
│   └── CRM_Data_Cleaning.ipynb
│
├── 04_Output
│   ├── CRM_Lead_Source_Performance.xlsx
│   ├── CRM_Industry_Performance.xlsx
│   ├── CRM_Country_Performance.xlsx
│   └── CRM_Deal_Size_Analysis.xlsx
│
├── 05_Screenshots
│   ├── 01_Final_Data_Validation.png
│   └── 02_Lead_Source_Performance.png
│
└── 06_Archive
    └── Project_3_CRM_Data_Cleaning_Raw.csv


Project Deliverables
- Cleaned CRM Dataset
- Python Data Cleaning Notebook
- Raw CRM Dataset
- Lead Source Performance Analysis
- Industry Performance Analysis
- Country Performance Analysis
- Deal Size Analysis
- Data Validation Screenshot
- Lead Source Performance Screenshot
- Business Analysis Case Study


Conclusion
This project demonstrates the complete process of transforming a raw CRM dataset into a reliable analytical asset.
The workflow covered data quality assessment, cleaning, validation, exploratory analysis, sales funnel analysis, performance segmentation, and business recommendation generation.
The analysis shows that referral and LinkedIn are important acquisition channels, Technology is a strong industry segment, the United Kingdom is a major market by associated deal value, and deal size alone is not sufficient to explain sales outcomes.
The project demonstrates practical skills in Python, Pandas, data cleaning, exploratory analysis, CRM analytics, and business insight generation.

---

## Data Privacy

The original CRM dataset contains customer-level information and is therefore excluded from this public repository.

Raw and cleaned customer-level datasets remain stored locally and are protected by `.gitignore`.

The repository contains the analytical code, documentation, aggregated outputs, screenshots, and case study needed to demonstrate the data-cleaning and analysis workflow without exposing customer information.