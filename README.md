# ⚡ EV Energy Use Simulation in Buffalo’s Snowy Terrain

**Simulation-Based Evaluation of Electric Vehicle Routes with Time Windows**

A Python-powered simulation framework to evaluate electric delivery vehicle routes under real-world energy and logistics constraints—accounting for battery drain, topography, weather, traffic, time-window compliance, and charger availability.

---

## 📌 Project Overview

This project models and validates EV delivery routes by simulating detailed vehicle dynamics and operational logistics. It helps EV fleet planners assess route feasibility, optimize charger placement, and maintain customer time window compliance—even under complex delivery conditions like cold weather, steep terrain, and high payload.

---

## 🎯 Key Capabilities

- 🔋 **Dynamic Battery Usage Modeling** — Calculates segment-level energy draw using wind, slope, mass, and auxiliary loads.
- 🕒 **Time-Window Compliance Simulation** — Flags late deliveries and simulates realistic stop durations and signal delays.
- ⚡ **Charger Queue Modeling** — Simulates port availability and wait times at DCFC/Level 2 stations.
- 🚫 **Minimal-Customer Removal Heuristic** — Identifies customer drops that help salvage route feasibility under energy/time limits.
- 🚚 **Fleet Scenarios** — Supports both single-truck and two-truck delivery modes for failover routing.

---

## 📁 Repository Structure

📦 ev-delivery-route-simulation.
├── src/ # Simulation engine & battery model code.
├── notebooks/ # Jupyter notebooks for analysis and visualization.
├── data/ # Sample telemetry and customer input data.
└── README.md # You are here.


---

## ⚙️ Technical Methodology

- **Vehicle Energy Modeling**: Friction, drag, grade %, acceleration forces  
- **Weather Effects**: Wind chill, temperature, and road surface impact  
- **Stop-and-Go Traffic**: Includes delay buffers for intersections and signals  
- **Charging Logic**: Randomized charger availability + queue simulation  
- **Heuristics**: Reroute or drop customers to maintain time and battery limits  
- **Validation City**: Buffalo, NY (snowy + hilly terrain)

---

## 📊 Results Summary

- Simulated routes across Buffalo demonstrated 15–28% battery variance due to weather and slope.
- Charging delays pushed 11% of routes over customer SLA unless rerouted.
- Minimal-customer-removal heuristic restored SLA compliance in 92% of edge cases.
- Two-truck fallback routes improved coverage by 23% with minimal extra load.

---

## 🚧 Future Enhancements

- Live traffic API integration (e.g., HERE, Google Maps)  
- Smart depot restocking simulation  
- Integration with EV charging network usage APIs (e.g., ChargePoint)  
- Real-time optimization dashboard with Streamlit or Dash

---

## 📜 License & Use

This repository is provided for research and educational use.  
Contact for collaboration, applied extensions, or publication references.
