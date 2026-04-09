# Restaurant Performance Evaluation and Customer Engagement Study

## 📌 Project Objective
This project analyzes restaurant performance, cuisine popularity, and customer engagement across multiple countries using Power BI.  
The goal is to:
- Identify top cuisines and geographic hotspots
- Evaluate customer ratings and votes
- Assess adoption of services such as online delivery and table booking
- Provide actionable insights for restaurant owners and food delivery platforms

---

## 📊 Data Sources
- **Dataset**: Zomato restaurant listings (cleaned and preprocessed in Excel)
- **Attributes**: RestaurantID, Name, Country, City, Cuisine, Rating, Votes, Price Range, Delivery, Table Booking, Coordinates, Month-Year
- **Domain**: Food & Hospitality

---

## 🛠️ Tools & Technologies
- **Microsoft Excel**: Data cleaning, transformation, handling duplicates, missing values
- **Power BI**: Data modeling, DAX measures, interactive dashboards, KPI computation, drill-down analysis

---

## 🧹 Data Pre-Processing
- Removed duplicates based on RestaurantID
- Standardized country and city names
- Handled missing ratings and votes
- Created calculated fields (Month-Year, Quarter)
- Converted categorical values (Delivery, Table Booking) into Yes/No flags

---

## 🗂️ Data Model
- **Fact Table**: Restaurant data (ratings, votes, services)
- **Dimension Tables**:  
  - Country dimension  
  - Cuisine dimension  
  - Calendar table (Month, Quarter, Year)
- Relationships: One-to-many joins between fact and dimensions

---

## 📐 Key DAX Measures
- **Average Rating** = AVERAGE(Restaurants[Rating])  
- **% Restaurants with Delivery** = DIVIDE(CALCULATE(COUNTROWS(Restaurants), Restaurants[Delivery] = "Yes"), COUNTROWS(Restaurants))  
- **Cuisine Popularity** = COUNTROWS(Restaurants) grouped by Cuisine  
- **% Restaurants with Table Booking**  
- **Votes per Restaurant**

---

## 📈 Dashboards
### 1. Restaurant Overview
- KPIs: Total Restaurants, Avg Rating, Total Votes, Countries, Cities
- Country-wise restaurant distribution
- City-wise restaurant counts

### 2. Rating Analysis
- Rating bucket distribution (1–2, 2–3, 3–4, 4–5)
- Insights into customer satisfaction trends

### 3. Service Adoption
- Donut chart: Table booking adoption
- Donut chart: Online delivery adoption

### 4. Cuisine Dashboard
- Cuisine-wise restaurant counts
- Ratings by cuisine
- Votes vs Rating for top brands

---

## 🔍 Insights & Conclusions
- India dominates with the highest restaurant count
- Majority of restaurants fall in the 3–4 rating range (moderate satisfaction)
- Online delivery is widely adopted, while table booking remains limited
- North Indian and Chinese cuisines are most popular, with international cuisines showing growth

**Prescriptive Insights:**
- Improve service quality to raise ratings in the 3–4 bucket
- Expand table booking services in high-demand cities
- Diversify cuisine offerings to capture new markets
- Strengthen delivery infrastructure in countries with lower adoption

---

## ✅ Conclusion
This project demonstrates end-to-end analytics using Excel and Power BI.  
The dashboards provide actionable insights for restaurant owners, food delivery platforms, and policymakers to improve customer satisfaction, expand services, and identify growth opportunities.
