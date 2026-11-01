# 📉 Customer Churn Analysis | Power BI 

![Power BI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=Power%20BI&logoColor=black)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)

This project explores customer churn behavior through interactive Power BI dashboards using a structured Excel dataset. The primary objective is to identify trends, pinpoint key churn drivers, and deliver actionable insights to improve customer retention strategies.

---

## 📊 Project Overview
Customer churn is a critical KPI for any financial or service-based business. This project analyzes churn patterns among bank customers across various dimensions, including credit card status, geography, age, gender, and credit scores. The dashboard provides dynamic visualizations to help stakeholders quickly spot at-risk segments and make data-driven decisions.

---

## 🛠️ Tools & Technologies
- **Power BI:** Data modeling, dynamic DAX measure creation, and interactive dashboard development.
- **Microsoft Excel:** Raw data storage, cleaning, and preparation.

**Project Files:**
- 👉 [Dashboard_1 Screenshot](./Dashboard_1.png)
- 👉 [Dashboard_2 Screenshot](./Dashboard_2.png)
- 👉 [Datasets Directory](./Datasets/)

---

## 📂 Data Modeling & Schema
The dataset is structured using a **Star Schema** to optimize query performance and reporting in Power BI. It consists of one central fact table surrounded by multiple dimension tables.

| Table Name       | Type | Key Columns |
|------------------|------|-------------|
| `Bank_Churn`     | Fact | `CustomerID`, `Age`, `Balance`, `CreditScore`, `Bank DOJ`, `Exited`, `EstimatedSalary`, `GenderID`, `CreditID`, `ExitID`, `GeographyID`, `ActiveID` |
| `CustomerInfo`   | Dim  | `CustomerID`, `Surname` |
| `ActiveCustomer` | Dim  | `ActiveID`, `ActiveCategory` |
| `ExitCustomer`   | Dim  | `ExitID`, `ExitCategory` |
| `CreditCard`     | Dim  | `CreditID`, `Category` |
| `Geography`      | Dim  | `GeographyID`, `GeographyLocation` |
| `Gender`         | Dim  | `GenderID`, `GenderCategory` |
| `Date Master`    | Dim  | `Date`, `Month`, `Month Order`, `Year` |

### 🗂️ Schema Diagram
![Schema Diagram](https://github.com/user-attachments/assets/02336bf6-d2bf-4cfa-84dc-0357ed8ff0c3)  
*ERD illustrating the one-to-many relationships between the dimension tables and the central fact table.*

---

## ❓ Key Business Questions Answered
1. What are the overall churn and retention rates?
2. How does the churn trend fluctuate across different years and months?
3. Which demographic segments (age, gender, geography) exhibit the highest exit rates?
4. Do credit card holders churn less frequently than non-holders?
5. Which credit score categories are most vulnerable to churn?

---

## 📈 Power BI Dashboards

### 1. Customer Churn Overview
Provides a high-level executive summary of customer demographics and overall churn metrics.  
![Overview Dashboard](https://github.com/user-attachments/assets/2fb36cde-c16f-4d2b-a03e-f8bf66609695)

### 2. Retention & Exit Trends
Dives deeper into behavioral trends, geographic distribution, and risk factors associated with exiting customers.  
![Trends Dashboard](https://github.com/user-attachments/assets/7737a2f2-7b51-4bd3-9e80-0c76470e9312)

---

## 🔍 Key Insights
- **Churn Rate:** Approximately **20%** of the customer base has exited the service.
- **Retention:** 7,963 out of 10,000 customers were successfully retained.
- **Geography:** France accounts for the highest absolute number of exited customers, while Germany and Spain demonstrate better retention ratios.
- **Age Factor:** The highest concentration of churn occurred among customers aged **30–45**.
- **Credit Score:** Customers categorized with "Fair" and "Poor" credit scores are significantly more prone to churning.
- **Credit Cards:** Non-credit card holders represent a disproportionately larger segment of churned customers.

---

## 🚀 How to Use This Repository
1. Clone the repository to your local machine.
2. Ensure you have [Power BI Desktop](https://powerbi.microsoft.com/desktop/) installed.
3. Open the `.pbix` file.
4. If prompted to refresh data, update the data source settings to point to your local `\Datasets\` directory.

---

## 📬 Contact

**Author**: Prince Kumar  
**LinkedIn**: https://www.linkedin.com/in/princeperspective/ 
**GitHub**: https://github.com/princeperspective

⭐ *Feel free to fork or star this repo if you found it useful!*