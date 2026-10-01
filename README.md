#**#✈️ Airline Passenger Experience & Operations Analytics**

## 📊 Project Overview

An interactive **Power BI dashboard** developed to analyze airline passenger experience, satisfaction, service quality, and flight operations.

This project transforms airline passenger survey data into meaningful **KPIs, business insights, and interactive visualizations** using Power BI and DAX.

---

## 🎯 Project Objectives

- Analyze overall passenger satisfaction
- Compare satisfaction across different travel classes
- Understand passenger demographics
- Analyze departure and arrival delays
- Evaluate airline service quality
- Study the relationship between flight distance and delays
- Analyze passenger experience across different customer segments
- Identify areas that can improve passenger experience

---

## 🛠️ Tools & Technologies

- **Power BI**
- **DAX**
- **Microsoft Excel / CSV**
- **Data Cleaning**
- **Data Visualization**
- **Exploratory Data Analysis (EDA)**
- **Business Analytics**
- **KPI Development**

---

## 📌 Key Performance Indicators (KPIs)

The dashboard tracks the following important KPIs:

- 👥 **Total Passengers**
- 😊 **Satisfied Passengers**
- ⭐ **Overall Satisfaction Rate**
- ⏱️ **Average Departure Delay**
- 🛬 **Average Arrival Delay**

---

## 📊 Dashboard Analysis

### 👤 Passenger Profile

The dashboard analyzes:

- Age
- Gender
- Customer Type
- Age Group

### ✈️ Travel Information

The analysis includes:

- Type of Travel
- Travel Class
- Flight Distance

### 😊 Satisfaction Analysis

The dashboard provides insights into:

- Overall Passenger Satisfaction
- Satisfied Passengers
- Dissatisfied Passengers
- Satisfaction Rate
- Satisfaction by Travel Class

### ⏱️ Delay Analysis

Flight operations are analyzed using:

- Departure Delay
- Arrival Delay
- Delay Category
- Delayed Passengers
- Average Departure Delay
- Average Arrival Delay

### 💺 Cabin Experience

Passenger experience is evaluated using:

- Seat Comfort
- Leg Room Service
- Inflight Service
- Inflight Entertainment

### 🍴 Onboard Services

The dashboard analyzes:

- Food & Drink
- Inflight Wi-Fi Service
- Online Boarding

### 🛫 Airport Services

Airport-related services include:

- Check-in Service
- Gate Location
- Baggage Handling

### 📏 Flight Performance

Operational performance is analyzed using:

- Flight Distance
- Departure Delay
- Arrival Delay
- Average Flight Delays

### 📋 Service Quality

Service ratings are analyzed across different travel classes using:

- Seat Comfort
- Cleanliness
- Food & Drink
- Inflight Service
- Online Boarding
- Inflight Wi-Fi
- Leg Room Service
- Check-in Service
- Baggage Handling

---

## 🧮 DAX Measures

### Total Passengers

```DAX
Total Passengers =
COUNTROWS(test)

**Satisfied Passengers**
Satisfied Passengers =
CALCULATE(
    [Total Passengers],
    test[Satisfaction] = "satisfied"
)

**Dissatisfied Passengers**
Dissatisfied Passengers =
CALCULATE(
    [Total Passengers],
    test[Satisfaction] = "neutral or dissatisfied"
)

**Satisfaction %**
Satisfaction % =
DIVIDE(
    [Satisfied Passengers],
    [Total Passengers],
    0
)

Average Flight Distance
Average Flight Distance =
AVERAGE(test[Flight Distance])

Average Departure Delay
Average Departure Delay =
AVERAGE(test[Departure Delay in Minutes])

Average Arrival Delay
Average Arrival Delay =
AVERAGE(test[Arrival Delay in Minutes])

Delayed Passengers
Delayed Passengers =
CALCULATE(
    [Total Passengers],
    test[Departure Delay in Minutes] > 0
)

Delay %
Delay % =
DIVIDE(
    [Delayed Passengers],
    [Total Passengers],
    0
)

Average Seat Comfort
Average Seat Comfort =
AVERAGE(test[Seat comfort])

🏷️ Calculated Columns
Age Group
Age Group =
SWITCH(
    TRUE(),
    test[Age] < 25, "Under 25",
    test[Age] < 35, "25-34",
    test[Age] < 45, "35-44",
    "45+"
)

Delay Category
Delay Category =
SWITCH(
    TRUE(),
    test[Departure Delay in Minutes] = 0, "No Delay",
    test[Departure Delay in Minutes] <= 15, "Short Delay",
    test[Departure Delay in Minutes] <= 60, "Medium Delay",
    "Long Delay"
)
📈 Power BI Visualizations

The dashboard includes multiple visualizations to provide different perspectives of the data:

📌 KPI Cards
📊 Column Chart – Satisfaction Rate by Class
🟦 Treemap – Passenger Distribution by Age Group
🍩 Donut Chart – Passenger Satisfaction Distribution
🔵 Scatter Chart – Flight Distance vs Departure Delay
🎯 Gauge – Overall Passenger Satisfaction
📋 Matrix – Service Quality Ratings
🔎 Interactive filtering using Power BI visual interactions
🔎 Key Business Questions

This dashboard helps answer questions such as:

What percentage of passengers are satisfied?
Which travel class has the highest satisfaction?
How are passengers distributed across different age groups?
What is the average departure delay?
What is the average arrival delay?
How does flight distance relate to departure delays?
Which service areas have stronger passenger ratings?
How does customer type relate to passenger satisfaction?
How does passenger experience vary across travel classes?
Which operational factors can be investigated to improve passenger satisfaction?
💡 Business Insights

The dashboard can help airline management and analysts:

Monitor passenger satisfaction levels
Identify differences between travel classes
Understand customer segments
Monitor flight delay performance
Evaluate service quality
Identify potential areas for service improvement
Support data-driven customer experience decisions
📷 Dashboard Preview

📂 Dataset

This project uses the Airline Passenger Satisfaction dataset available on Kaggle.

Dataset Source:

https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction

The dataset contains passenger demographic information, travel details, flight delays, service ratings, and passenger satisfaction information.

📁 Project Structure
airline-passenger-experience-analytics/
│
├── README.md
│
├── Dashboard/
│   └── Airline_Dashboard.png
│
├── Dataset/
│   └── airline_passenger_satisfaction.csv
│
├── PowerBI/
│   └── Airline_Passenger_Experience_Analytics.pbix
│
└── Documentation/
    └── DAX_Measures.md
🚀 Skills Demonstrated

Power BI | DAX | Data Analysis | Data Visualization | Business Intelligence | Exploratory Data Analysis | KPI Development | Dashboard Development | Customer Experience Analytics

**👩‍💻 Author
Girisha Thangavalu**
🔗 GitHub:
https://github.com/Girishaa-12

⭐ Project Highlights
Interactive Power BI dashboard
DAX-based KPI calculations
Passenger satisfaction analysis
Flight delay analysis
Customer segmentation
Service quality analysis
Operational performance analysis
Business-focused data visualization
📌 Conclusion

The Airline Passenger Experience & Operations Analytics project demonstrates how Power BI and DAX can be used to convert passenger survey data into an interactive business intelligence solution.

The dashboard combines customer experience, service quality, passenger demographics, and flight operations in a single analytical view to support data-driven decision-making.
