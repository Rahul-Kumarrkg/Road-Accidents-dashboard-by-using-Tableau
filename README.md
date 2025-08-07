## 🚧 **Road Accidents Analysis Dashboard using Tableau**

---

## 🎯 Objective:

To analyze road accident data to identify trends, causes, locations, and potential solutions. This dashboard helps traffic authorities and policy makers take data-driven decisions to reduce accidents.


---

## 📂 Dataset:

You can use publicly available datasets, such as:

* Government open data portals (India: [https://data.gov.in/](https://data.gov.in/))
* UK Road Safety Data
* Kaggle: [Road Accident Data](https://www.kaggle.com/datasets)

### Typical Fields:

* `Date`, `Time`, `Day of Week`
* `Location`, `State`, `City`
* `Number of Casualties`, `Severity` (Fatal, Serious, Slight)
* `Vehicle Type`, `Weather Conditions`, `Road Surface`
* `Cause of Accident`, `Speed`, `Alcohol Involved`

---

## 🧠 Key Questions to Answer:

1. Which states or cities have the highest number of accidents?
2. What time of day are accidents most common?
3. Which factors contribute the most to severe accidents?
4. What is the trend over the years?
5. Which vehicle types are most involved in accidents?

---

## 🛠️ Step-by-Step Project Flow in Tableau

### 🔹 Step 1: Load the Dataset

* Open Tableau Desktop.
* Connect to your `.csv`, `.xlsx`, or database file.
* Drag and drop required tables into the Data pane.
* Inspect and clean the data (fix dates, remove nulls, etc.).

---

### 🔹 Step 2: Create Calculated Fields

Examples:

```tableau
Year = YEAR([Date])
Month = MONTH([Date])
Hour = HOUR([Time])
```

```tableau
Severity Category = 
IF [Severity] = 'Fatal' THEN 'High'
ELSEIF [Severity] = 'Serious' THEN 'Medium'
ELSE 'Low'
END
```

---

### 🔹 Step 3: Build the Dashboard Visuals

#### 📈 1. **Trend Over Time**

* **Line Chart**

  * X-Axis: `Year` or `Month`
  * Y-Axis: `Count of Accidents`
  * Show trend of accidents increasing or decreasing

#### 📊 2. **Severity Breakdown**

* **Stacked Bar / Pie Chart**

  * Breakdown of Fatal, Serious, Slight accidents
  * Helps prioritize interventions

#### 🗺️ 3. **Accident Map**

* **Filled Map or Symbol Map**

  * Use `Latitude` and `Longitude` or `State/City`
  * Color based on total accidents or fatalities

#### 📅 4. **Accidents by Time**

* **Heat Map**

  * X: Day of Week
  * Y: Hour of Day
  * Color: Number of accidents
  * Reveals peak accident hours

#### 🚗 5. **Vehicle Type Analysis**

* **Bar Chart**

  * Vehicle types vs Number of Accidents
  * Helps target vehicle safety awareness (e.g., bikes or trucks)

#### 🌦️ 6. **Weather or Road Condition**

* **TreeMap or Bar Chart**

  * Accident counts per road condition or weather type

---

### 🔹 Step 4: Create Filters and Interactivity

* **Dropdown filters**: Year, State, Vehicle Type, Severity
* **Highlight actions**: Click on a state to see detailed breakdown
* **Dashboard filters**: All charts update dynamically when filter is applied

---

### 🔹 Step 5: Design the Final Dashboard

### 🖥️ Dashboard Layout Idea:

| Section    | Visual                                   |
| ---------- | ---------------------------------------- |
| KPIs       | Total Accidents, Fatalities, Casualties  |
| Top Row    | Line Chart (Yearly Trend) + Severity Pie |
| Middle     | Accident Map + Time Heatmap              |
| Bottom     | Vehicle Type Bar + Weather TreeMap       |
| Side Panel | Filters: Year, Region, Vehicle Type      |

---

## 🔍 Example Insight You Can Show:

| Year | Accidents | Fatalities | YoY Change |
| ---- | --------- | ---------- | ---------- |
| 2019 | 12,500    | 3,200      | -          |
| 2020 | 10,800    | 2,900      | ▼ -13.6%   |
| 2021 | 14,300    | 3,500      | ▲ +32.4%   |
| 2022 | 15,200    | 3,800      | ▲ +6.3%    |

---

## 📤 Final Output:

* An interactive **Tableau Dashboard (.twb/.twbx)** file
* Publishable to **Tableau Public** or **Tableau Server**
* Used by **Government agencies, NGOs, City Planners**

---

## 💡 Bonus Features:

* Add **trend forecast** using Tableau’s **Analytics Pane**
* Create **dynamic drill-down** (e.g., State → City → Street)
* Export dashboards to PDF/Excel for reporting
* Add **color-coded alerts** for high-risk regions

---

## 📌 Tools Used:

* **Tableau Desktop** (for design)
* **Tableau Public** (for sharing)
* **Excel / CSV** (as source)

---


## 📍 Project Summary:
This project focused on developing a dynamic and insightful Tableau dashboard to analyze and visualize road accident data across multiple years. The primary goal was to uncover critical patterns, trends, and risk factors contributing to accidents, helping authorities and planners make informed decisions for improving road safety.

---

## ✅ Outcome:
The dashboard provided actionable insights to support road safety strategies, such as targeted infrastructure upgrades, time-specific traffic enforcement, vehicle-type awareness campaigns, and data-driven policy formulation.

<img src="Road Accident DashBoard.png" width="1000"/>
