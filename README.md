# Daikibo Factory Telemetry Analysis Dashboard

## 📊 Project Overview

This project analyzes telemetry data collected from *Daikibo's four factories* over the month of *May 2021*. The objective was to identify:

1. *Which factory experienced the most machine downtime*
2. *Which machines contributed most to the downtime in that factory*

The analysis was conducted using *Tableau Desktop*.

---

## 🏭 Data Source

*Telemetry Data* collected from:

- Daikibo Factory Meiyo (Tokyo, Japan)
- Daikibo Factory Seiko (Osaka, Japan)
- Daikibo Berlin (Berlin, Germany)
- Daikibo Shenzhen (Shenzhen, China)

*Details:*

- 9 types of machines at each location
- Machines sent a message every 10 minutes
- Data format: daikibo-telemetry-data.json

---

## 🛠 Tools Used

- *Tableau Desktop* (Free Trial)
- Windows Operating System

---

## 📝 Analysis Steps

1. *Data Import*
   - Imported the JSON telemetry data into Tableau.

2. *Calculated Measure*
   - Created a calculated field named Unhealthy:
     tableau
     IF [status] = "unhealthy" THEN 10 ELSE 0 END
     
     This field quantifies downtime in minutes.

3. *Visualization 1: Down Time per Factory*
   - Bar chart showing total downtime (sum of Unhealthy) for each factory.

4. *Visualization 2: Down Time per Device Type*
   - Bar chart showing total downtime by device type.

5. *Dashboard*
   - Combined both charts into a single dashboard.
   - Configured *Down Time per Factory* as a *filter*, enabling interactive selection of factories.

6. *Selection*
   - Selected the factory with the highest downtime.
   - Captured a screenshot of the final dashboard highlighting the most affected devices in that factory.

---


---

## 📂 Repository Contents

- daikibo-telemetry-data.json – Raw telemetry data
- daikibo-telemetry-dashboardg.png – Screenshot of the Tableau dashboard
- README.md – This documentation

---


  
---

## ✨ Key Insights

- The factory with the highest total downtime can be identified interactively.
- The specific machine types responsible for downtime are clearly visualized.

---

