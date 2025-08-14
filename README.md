# AtliQ Grands Market Share Recovery Dashboard

## 📑 Quick Links
1. [About AtliQ Grands](#-about-atliq-grands)
2. [Project Overview](#-project-overview)
3. [Problem Statement](#-problem-statement)
4. [Data Sources](#-data-sources)
5. [Data Dictionary](#-data-dictionary)
6. [Tools & Technologies Used](#-tools--technologies-used)
7. [Dashboard Preview](#-dashboard-preview)
8. [Insight Generation](#-insight-generation)
9. [Recommendations](#-recommendations)
10. [How to Use](#-how-to-use)


##  <img width="70" height="50" alt="atliq-a-logo-04" src="https://github.com/user-attachments/assets/989aab88-8673-4b6e-9f1d-19c9e54a1bf7" /> About AtliQ Grands
AtliQ Grands is a premium hospitality chain operating in the luxury and business hotel segment, with over 20 years of experience in the industry. Known for delivering exceptional guest experiences, the company manages multiple upscale properties across 5 cities in India.

**Focus Areas:**
- Delivering high-quality service in the hospitality and tourism industry.
- Continuously improving operational efficiency.
- Enhancing guest satisfaction through data-driven decision-making.
- Optimizing costs, increasing revenue, and maintaining high occupancy rates across departments (Front Office, Housekeeping, Room Service, Food & Beverages).

---

## 📊 Project Overview
AtliQ Grands faced a steady decline in market share due to strong competitor strategies and internal decision-making gaps.  
This **Power BI** project analyzes performance across cities, room categories, and booking platforms to uncover:
- Revenue patterns
- Occupancy gaps
- Operational inefficiencies

**Key metrics tracked:** Revenue, Occupancy %, ADR (Average Daily Rate), RevPAR (Revenue Per Available Room).  

The dashboard equips management with **actionable insights** to:
- Enhance occupancy
- Reduce cancellations
- Improve guest ratings
- Strengthen competitive positioning in the luxury and business hotel segments


---

## ❗ Problem Statement
AtliQ Grands, a leading player in the luxury and business hotel sector, has been experiencing a steady decline in market share and revenue due to aggressive competitive strategies and ineffective internal decision-making.  

Despite having a strong presence in key cities, the chain faces:
- Inconsistent occupancy rates
- High cancellation percentages
- Declining guest satisfaction in certain properties
- Over-reliance on the luxury segment

Without a clear, data-driven understanding of these performance gaps, management risks further erosion of its competitive position in the hospitality market.

---

## 🗂 Data Sources
1. **dim_date** – Calendar details (date, month-year, week no, day type).
2. **dim_hotels** – Hotel details (property ID, name, category, city).
3. **dim_rooms** – Room type and class.
4. **fact_aggregated_bookings** – Aggregated bookings and room capacity.
5. **fact_bookings** – Individual booking details, guest info, revenue, and booking status.
6. [View the Codebasics Resume Project Challenge](https://codebasics.io/challenges/codebasics-resume-project-challenge/4)

---

## 📋 Data Dictionary

**`dim_date`**
- `date` – Dates for May, June, and July.
- `mmm yy` – Month-year format.
- `week no` – Unique week number.
- `day_type` – Weekend or Weekday.

**`dim_hotels`**
- `property_id` – Unique hotel ID.
- `property_name` – Name of the hotel.
- `category` – Luxury or Business.
- `city` – Location of the hotel.

**`dim_rooms`**
- `room_id` – Room type ID.
- `room_class` – Standard, Elite, Premium, or Presidential.

**`fact_aggregated_bookings`**
- `property_id` – Unique hotel ID.
- `check_in_date` – Guest check-in date.
- `room_category` – Room type (RT1, RT2, RT3, RT4).
- `successful_bookings` – Number of successful bookings.
- `capacity` – Maximum available rooms for that date and type.

**`fact_bookings`**
- `booking_id` – Unique booking ID.
- `property_id` – Unique hotel ID.
- `booking_date` – Date of booking.
- `check_in_date` / `check_out_date` – Guest stay dates.
- `no_guests` – Number of guests.
- `room_category` – Room type.
- `booking_platform` – Channel used for booking.
- `ratings_given` – Guest rating for services.
- `booking_status` – Cancelled, Checked Out, or No Show.
- `revenue_generated` – Total amount charged.
- `revenue_realized` – Amount earned after deductions/refunds.

---

## 🛠 Tools & Technologies Used
- **Power BI** – Created interactive dashboard, tracked KPIs, and enabled drill-down analysis.
- **Microsoft Excel** – Initial data cleaning, formatting, and exploratory analysis.
- **DAX (Data Analysis Expressions)** – Calculated columns and measures (RevPar, occupancy rate, revenue growth %).
- **Data Modelling** – Built relationships between multiple datasets for efficient analysis.
- **Visualization Techniques** – Used bar charts, line graphs, KPI cards, and slicers for interactive storytelling.

---

## 🔍 Insight Generation

### **Revenue & Occupancy Performance**
- Total Revenue: ₹1.71B (**+7.23% WoW**), but occupancy fell **0.96%** to 57.9%.
- RevPar decreased **0.93% WoW** to ₹7,350 despite stable ADR (+0.03%).
- DSRN increased **8.24% WoW** — capacity grew, but underutilized.

### **Category-Wise Revenue Split**
- Luxury: ₹1.05B (**61.6%**)
- Business: ₹0.66B (**38.4%**) → Over-reliance on luxury.

### **Weekday vs Weekend Trends**
- Weekday revenue: ₹1.28B, occupancy 58.6%.
- Weekend revenue: ₹0.43B, occupancy 55.7%.
- ADR stable — price not driving occupancy changes.

### **Platform Performance**
- Highest ADR: Direct Offline (₹12,791)
- Lowest ADR: Direct Online (₹12,634)
- Lowest Realisation %: Tripster (69.83%)

### **Operational Pain Points**
- High cancellation rates (>25% at multiple properties).
- 6+ properties rated ≤3.1 → guest dissatisfaction risk.
- Occupancy <60% even in high-ADR cities.

### **City & Property Performance**
- Top 3 revenue properties all in Mumbai (₹118.45M, ₹101.51M, ₹94.00M) → 18.5% of total revenue.
- ADR gap: ₹8,677.68 (Hyderabad) vs ₹16,606.10 (Mumbai) → 91% difference.
- Several properties rated <3.0 (Mumbai, Hyderabad, Bangalore).

---

## 📷 Dashboard Preview
![Dashboard Preview](dashboard_screenshot.png)

## 💡 Recommendations
-	**Boost Occupancy with Targeted Campaigns**: Launch weekend-focused promotions and corporate travel packages for business hotels to close the 3%+ occupancy gap between weekdays and weekends, while leveraging        underutilized capacity (DSRN up 8.24% WoW).
-	**Diversify Revenue Sources**: Reduce reliance on the luxury segment (61.6% of revenue) by increasing business-category offerings, such as mid-tier rooms, meeting facilities, and bundled corporate services.
-	**Improve Guest Satisfaction & Ratings**: Prioritise service quality upgrades for low-rated properties (≤3.0 average rating), especially in Hyderabad, Bangalore, and certain Mumbai properties, to strengthen         repeat bookings and brand trust.
-	**Reduce Cancellations & No-Shows**: Implement flexible booking policies, targeted pre-stay engagement, and loyalty incentives to cut cancellation rates (>25% in multiple properties), which directly impact          revenue stability.
-	**Optimise Pricing & Platform Efficiency**: Re-evaluate ADR strategy in cities with high ADR but low occupancy (<60%) to align pricing with demand, and improve conversion efficiency on weaker platforms like         “tripster” (Realisation % 69.83%).


---

## 📂 How to Use
1. Download the `.pbix` file from this repository.
2. Open in **Power BI Desktop**.
3. Explore insights via slicers and filters.
4. Data model and measures can be found in the Power BI fields pane.

---

