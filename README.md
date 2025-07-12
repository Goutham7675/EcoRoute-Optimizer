# Green-Route-Planner-with-EV-Priority-Emission-Budgeting
Green Route Planner with EV Priority &amp; Emission Budgeting
# At present I've deleted previously uploaded files as I'm fixing minor bugs in this project, I'm working on the project to optimize the REST-APIs, Map API
# I'll upload the project files after a few days 
# 🌱 Green Route Planner with EV Priority & Emission Budgeting

A smart, AI-powered logistics route planner designed to optimize vehicle routing for environmental sustainability. This tool prioritizes Electric Vehicles (EVs), adheres to a defined carbon emissions budget, avoids traffic congestion using real-time data, and delivers optimized, eco-conscious logistics solutions for both EVs and Internal Combustion Engine (ICE) vehicles.

---

## 🚀 Project Goals

- **Optimize delivery routes** to reduce fuel consumption and travel time.
- **Prioritize EV-friendly paths**, incorporating charging infrastructure.
- **Adhere to per-route carbon emission budgets** for greener logistics.
- **Use real-time traffic data** to avoid congestion and delays.
- **Support mixed vehicle fleets** (EV and ICE) with intelligent routing.

---

## 🛠️ Technology Stack

| Component                  | Technology         |
|---------------------------|--------------------|
| VRP Solver                | OptaPlanner (Java) |
| Routing Engine            | GraphHopper        |
| Map Data                  | OpenStreetMap      |
| Real-Time Traffic         | HERE, TomTom, or Google Maps API |
| EV Charging API           | Open Charge Map, Chargetrip, ChargePoint |
| Refueling Station Data    | OSM, GasBuddy API  |
| Emissions Calculation     | Searoutes CO2 API, CarbonSmart |
| Programming Language      | Java               |
| Database (Optional)       | H2 / PostgreSQL    |
| Frontend (MVP)            | HTML/CSS/JS        |
| Build Tools               | Maven / Gradle     |
| IDE                       | IntelliJ / Eclipse |

---

## 📦 Features

### ✅ Core Routing
- Solves complex Vehicle Routing Problems (VRP) with capacity and time window constraints.
- Visualizes optimized routes using GraphHopper and OSM data.

### ♻️ Green Features
- **Carbon Emissions Budgeting:** Calculate and enforce route-based emissions limits.
- **EV-Aware Routing:** Integrates charging stops based on vehicle range and battery state.
- **ICE Optimization:** Plans efficient fuel usage and schedules refueling stops.
- **Real-Time Traffic Avoidance:** Dynamically adjusts road segment weights based on traffic conditions.

### 📍 Vehicle Profiles
- Custom profiles for each vehicle type:
  - **EVs**: max range, battery charge, charging speed, connector type.
  - **ICEs**: fuel tank, current fuel, efficiency metrics.

---

## 📁 Project Structure

```bash
green-route-planner/
├── docs/                   # Documentation & reports
├── src/                    # Java source files
│   ├── domain/             # OptaPlanner domain models
│   ├── solver/             # Constraint logic and solver config
│   └── services/           # GraphHopper integration, APIs
├── resources/              # OSM map files, config, static assets
├── frontend/               # Web UI (HTML/JS/CSS)
├── scripts/                # Setup and automation scripts
├── pom.xml / build.gradle  # Dependency manager
└── README.md               # Project overview
```
### ⚙️ Setup Instructions
## 1. Environment Setup
Install Java 11+

Install Maven or Gradle

Clone this repo and open in IntelliJ / Eclipse

## 2. Dependencies
Add OptaPlanner and GraphHopper dependencies in pom.xml or build.gradle.

## 3. GraphHopper Setup
bash
Copy
Edit
# Download OSM data
wget https://download.geofabrik.de/asia/india-latest.osm.pbf

# Build GraphHopper routing graph
java -jar graphhopper-web-*.jar import india-latest.osm.pbf
4. Run the Solver
Define delivery points, depots, and vehicles in input files or UI.

Execute the OptaPlanner solver via main().

🧠 Key Concepts
OptaPlanner
Solves the VRP by minimizing:

Total distance/time

Number of vehicles used

Emissions (as soft constraints)

Enforces:

Capacity constraints

Time windows

Emission budget (as hard constraint)

GraphHopper
Calculates road distances and travel times.

Customizable routing based on vehicle profiles and real-time traffic.

📈 Future Enhancements
Add REST API for backend/frontend communication.

Improve frontend with React/Leaflet.js.

Integrate with fleet/order management systems.

Implement predictive traffic using historical data.

Extend emissions modeling with dynamic engine load data.

🧩 APIs Used (with Free Tier Access)
Traffic: HERE / TomTom / Google Maps

Charging Stations: Open Charge Map / Chargetrip / ChargePoint

Fuel Stations: OpenStreetMap POIs / GasBuddy

Carbon Emissions: Searoutes CO2 / CarbonSmart API

📜 License
This project uses only open-source tools and data:

OptaPlanner – Apache License 2.0

GraphHopper – Apache License 2.0

OpenStreetMap – Open Data License

👥 Contributors
**Goutham Reddy**

Tech Stack: Java, OptaPlanner, GraphHopper, OpenStreetMap

Domain: Logistics Optimization, Green Tech, AI Routing

🌍 Impact
This project aims to help organizations:

Cut logistics emissions

Improve delivery efficiency

Transition to sustainable transport

