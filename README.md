## 💳 Credit Card Financial Dashboard | Power BI

> Interactive Power BI dashboard analyzing credit card customer spending 
> behavior, credit utilization, payment trends, and risk indicators using 
> DAX and Star Schema modeling.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Power Query](https://img.shields.io/badge/Power%20Query-217346?style=for-the-badge&logo=microsoft&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

---

## 📸 Dashboard Preview

![Customer Dashboard](credit_card_customer_dashboard.jpg)
![Transaction Dashboard](credit_card_transaction_dashboard.jpg)

---

## 📌 Project Overview

| Detail      | Info                                        |
|-------------|---------------------------------------------|
| Tool        | Power BI Desktop                            |
| Data Source | credit_card.csv + customer.csv              |
| Techniques  | DAX, Power Query, Star Schema Modeling      |
| Domain      | Financial Services / Banking                |
| Status      | ✅ Completed                                |

---

## 🎯 Key Features

- 📊 Interactive slicers for customer segment, card category, and time period
- 💡 DAX measures for KPI calculations — credit utilization ratio, payment rate, outstanding balance
- 🗂️ Star schema data modeling linking customer and transaction tables
- ⚠️ Risk indicator flags for high-utilization customers
- 📈 Spending trend analysis over time by category and card type
- 👥 Customer segmentation by demographics and spending behavior

---

## 🔍 Key Insights

- Category-wise spending distribution across all card types
- Credit utilization trends — identifying high-risk customer segments
- Payment behavior analysis — On-time vs Late payment patterns
- Outstanding balance monitoring with risk-based segmentation
- High-value customer identification to support targeted business strategies

---

## 🧮 DAX Measures Used
```dax
-- Credit Utilization Rate
Credit Utilization Rate = 
DIVIDE(SUM(credit_card[outstanding_balance]), 
       SUM(credit_card[credit_limit]), 0)

-- Payment Rate
Payment Rate % = 
DIVIDE(SUM(credit_card[total_payment]),
       SUM(credit_card[total_due]), 0) * 100

-- High Risk Customers
High Risk Customers = 
CALCULATE(COUNTROWS(customer),
          credit_card[utilization_rate] > 0.75)

-- Total Outstanding Balance
Total Outstanding = SUM(credit_card[outstanding_balance])
```

---

## 📂 Project Structure
```
├── Credit Card Report.pbix                   # Power BI dashboard file
├── Credit_Card_Dashboard_Presentation.pptx  # Stakeholder presentation
├── credit_card_customer_dashboard.jpg        # Dashboard screenshot 1
├── credit_card_transaction_dashboard.jpg     # Dashboard screenshot 2
├── credit_card.csv                           # Transaction dataset
├── customer.csv                              # Customer dataset
└── README.md                                 # Project documentation
```

---

## ▶️ How to Use

1. Download **Power BI Desktop** (free) from [microsoft.com](https://powerbi.microsoft.com/desktop/)
2. Clone this repository
```bash
   git clone https://github.com/DebashisSen2025/credit-card-sales-analysis-crio.git
```
3. Open `Credit Card Report.pbix` in Power BI Desktop
4. Explore the dashboard using slicers and filters
5. View `Credit_Card_Dashboard_Presentation.pptx` for a summarized insight report

---

## 👋 About Me

**Debashis Sen** | Data Analyst

🏆 HackerRank SQL — 5 Star (Advanced Certified)  
📊 11+ real-world analytics projects | Crio.do NextGen Data Analytics Fellowship  
📍 Jamshedpur, India | Immediate Joiner  

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Debashis_Sen-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/debashis-sen25)
[![GitHub](https://img.shields.io/badge/GitHub-DebashisSen2025-black?style=flat&logo=github)](https://github.com/DebashisSen2025)
[![Email](https://img.shields.io/badge/Email-sen.debashis.sd@gmail.com-red?style=flat&logo=gmail)](mailto:sen.debashis.sd@gmail.com)

---

⭐ If you found this project useful, please consider giving it a star!
