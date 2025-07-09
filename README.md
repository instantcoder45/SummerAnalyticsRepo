# SummerAnalyticsRepo
##  Dynamic Parking Pricing Simulation using Pathway

### 🚀 Project Overview

This project simulates a real-time dynamic pricing model for urban parking spaces using streaming data and the [Pathway](https://pathway.com/) framework. 

Data was collected from **14 parking spaces** over **73 days**, captured at **30-minute intervals** from 8:00 AM to 4:30 PM. The system computes dynamic prices based on features such as occupancy, queue length, vehicle type, traffic congestion, and special days.

The final output is visualized live using Bokeh and Panel to emulate real-world pricing changes for each parking lot.

---

### 🛠 Tech Stack

| Tool / Library | Purpose |
|----------------|---------|
| **Python** | Programming Language |
| **Pathway** | Real-time streaming data processing |
| **Pandas / NumPy** | Data manipulation |
| **Matplotlib** | Static visualization |
| **Bokeh** | Interactive visualizations |
| **Panel** | Web app interface |
| **Google Colab** | Development & experimentation |

---

### 🧠 Architecture Diagram
![Screenshot 2025-07-10 032749](https://github.com/user-attachments/assets/eea4a78c-901c-41be-adcf-046210450601)

---
## 🔧 Project Workflow (Simplified)

1. **Data Preparation**  
   - Converted timestamp strings into datetime objects.  
   - Encoded vehicle types numerically and computed key features like `fill_percent` (occupancy/capacity).

2. **Demand Estimation**  
   - Built a weighted formula incorporating multiple real-time features.  
   - Applied rolling averages and normalization for stability in pricing.

3. **Real-Time Processing with Pathway**  
   - Simulated a streaming pipeline using Pathway.  
   - Used `.with_columns()` to dynamically compute prices as new data arrived.

4. **Dynamic Pricing Logic**  
   - Final price = Base price × (1 + λ × Demand).  
   - Prices were calculated independently for cycle, bike, car, and truck.

5. **Interactive Visualization**  
   - Real-time price plots built with Bokeh and Panel.  
   - All vehicle types plotted simultaneously for comparison.

6. **Competitor & Location Analysis**  
   - Used latitude-longitude data for spatial comparison of lots.  
   - Identified pricing gaps and demand inefficiencies between nearby spaces.

---

## 📄 Included Documentation

- This repository contains a detailed **project report** describing the methodology, model logic, exploratory analysis, and observations.
- Collab link to model 1: https://colab.research.google.com/drive/1V20xS57JNRAbbbVAS455ApSR0e7nNtUD?usp=sharing
- Collab link to model 2: https://colab.research.google.com/drive/1PhzI4Br0OrHfnD72zizsNAYA1G4_MOFP?usp=sharing

---

## 🙏 Final Note

This was my **first full-fledged data science project**, and it helped me gain hands-on experience in real-time analytics, feature engineering, and building interactive dashboards. Thank you for checking it out!
