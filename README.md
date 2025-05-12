**💳 Global Card Fraud Risk Analysis Dashboard**

A comprehensive Power BI data visualization tool designed to uncover and analyze global card fraud patterns across multiple dimensions.

**Purpose**
The Global Card Fraud Risk Analysis Dashboard is an interactive Power BI report created to transform raw financial security data into actionable insights. By leveraging a Kaggle dataset, the dashboard provides a multi-dimensional view of card fraud risks, enabling deeper understanding of fraudulent transaction patterns.
Tech Stack

📊 Power BI Desktop – Primary data visualization platform
📂 Power Query – Data transformation and cleaning
🧠 DAX (Data Analysis Expressions) – Custom calculations and measures
📁 File Format – .pbix for development, .png for dashboard previews

**Data Source**
Source: Kaggle Card Fraud Risk Analysis Dataset
Comprehensive dataset covering card fraud transactions with detailed information on fraud flags, transaction amounts, card types, and risk levels.
Features & Highlights
Business Problem
Financial institutions and security teams struggle to quickly identify and understand complex fraud patterns across different dimensions such as merchant types, card types, and geographic regions.

**Key Insights**

Overall fraud rate: 50.5%
Total fraudulent transactions: 303
Fraudulent transaction amount: $792.73K
High-risk transactions: 34.00%
Countries analyzed: 6

**Dashboard Capabilities**

Detailed fraud flag analysis by merchant type and card type
Geographic distribution of fraudulent transactions
Risk level breakdown of total transaction amounts
Comprehensive filtering options for deep-dive analysis

**Key Visualizations**

Fraud Flags by Merchant and Card Type
Fraudulent Transactions by Country
Total Transaction Amount by Risk Level
Fraudulent Transactions by Card Type

**Business Impact**

Enables rapid identification of high-risk transaction patterns
Supports targeted fraud prevention strategies
Provides multi-dimensional view of fraud risks
Assists in developing more robust financial security measures

**DAX Measures**
daxFRAUD RATE % = DIVIDE('card_risk_analysis_dataset'[FRAUDULENT TRANSACTION],COUNTROWS('card_risk_analysis_dataset'),0)*100
FRAUDULENT TRANSACTION = CALCULATE(COUNTROWS('card_risk_analysis_dataset'),'card_risk_analysis_dataset'[Fraud Flag] = 1)
FRAUDULENT TRANSACTION AMOUNT = CALCULATE([TOTAL AMOUT TRANSACTION],'card_risk_analysis_dataset'[Fraud Flag]=1)
HIGH RISK TRANSACTION = DIVIDE(CALCULATE(COUNTROWS('card_risk_analysis_dataset'),'card_risk_analysis_dataset'[Risk Level]="High"),COUNTROWS('card_risk_analysis_dataset'),0)*100
TOTAL AMOUT TRANSACTION = SUM('card_risk_analysis_dataset'[Amount Spent (USD)])

**Screenshots**
Link : 'https://github.com/domybestttt/GLOBAL-CARD-FRAUD-RISK-ANALYSIS-DASHBOARD/blob/main/Screenshot%202025-05-12%20181618.png'
