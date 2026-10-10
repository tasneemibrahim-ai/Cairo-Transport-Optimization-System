# 🚀 Cairo Transport Optimization System

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)](https://streamlit.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Welcome to the **Cairo Transport Optimization System**, a smart planning and analysis tool built with Streamlit. This application is designed to model, analyze, and improve the public and private transportation networks across Greater Cairo using graph theory algorithms, network analysis, and interactive mapping.

## 📖 Table of Contents
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Algorithms Used](#-algorithms-used)
- [Project Structure](#-project-structure)
- [Datasets](#-datasets)
- [Installation & Setup](#-installation--setup)
- [How to Use](#-how-to-use)
- [Impact](#-impact)

## 🌟 Features

*   **🛣️ Road Network Visualization:** Interactive maps visualizing the current and proposed road networks with interactive overlays.
*   **🌉 MST Road Network:** Computes and visualizes the Minimum Spanning Tree (MST) for the road network to optimize construction costs and total road distance.
*   **🚦 Traffic Flow Optimization:** Identifies the most efficient driving routes considering real-time traffic conditions across different time periods (Morning, Afternoon, Evening, Night). Includes congestion analysis and alternate route suggestions.
*   **🚑 Emergency Routing:** Computes the fastest response paths for emergency services to reach hospitals, factoring in traffic conditions and traffic signal preemption to save lives.
*   **🚍 Public Transit Optimization:** Suggests optimal routes using multiple transit modes (Bus, Metro, Walking), minimizing travel time and transfer penalties.

## 🛠️ Tech Stack

*   **Python:** Core programming language.
*   **Streamlit:** Web application framework for the interactive user interface.
*   **Pandas:** Data manipulation, reading, and processing of CSV datasets.
*   **NetworkX:** Graph modeling and core routing algorithms (Dijkstra, A*, Kruskal's).
*   **Folium & Streamlit-Folium:** Interactive map generation and geospatial visualization.
*   **Matplotlib:** Plotting graphs, charts, and basic network visualizations.

## 🧠 Algorithms Used

This system leverages core computer science algorithms applied to geospatial graphs:
1.  **Dijkstra’s Algorithm:** Used for **Traffic Flow Optimization** to find the absolute shortest/fastest path between two neighborhoods considering varying edge weights (traffic).
2.  **A* Search Algorithm:** Used for **Emergency Routing**. By incorporating geographic heuristics (straight-line distance), it efficiently finds the fastest route to the nearest hospital.
3.  **Kruskal’s Algorithm:** Used for the **MST Road Network**. It computes the Minimum Spanning Tree to evaluate the bare minimum infrastructure required to connect all neighborhoods.
4.  **Dynamic Programming / Modified Shortest Path:** Used in **Public Transit Optimization** to factor in multi-modal transfers and frequencies.

## 📁 Project Structure

```text
├── main.py                   # Main Streamlit application with all pages and UI logic
├── Read.py                   # Auxiliary script for specific data reading tasks
├── cairo_traffic_map.html    # Pre-generated Folium interactive map
├── README.md                 # Project documentation
└── *.csv                     # Datasets (see below)
```

## 📊 Datasets

The system relies on various interlinked CSV datasets representing Cairo's infrastructure:
*   `neighborhoods.csv` & `area_names.csv`: Demographics, types, and coordinates of distinct areas.
*   `existing_roads.csv` & `new_roads.csv`: Edges of the road network, including distances and costs.
*   `traffic_flow.csv`: Temporal volume data for edges across different times of the day.
*   `facilities.csv`: Locations of key facilities (hospitals, fire stations).
*   `bus_routes.csv` & `metro_lines.csv`: Public transit routes and frequencies.
*   `transport_demand.csv`: Demand metrics.

## ⚙️ Installation & Setup

1.  **Clone the repository** (if applicable):
    ```bash
    git clone https://github.com/yourusername/Smart_City_Transportation.git
    cd Smart_City_Transportation
    ```

2.  **Create a Virtual Environment** (recommended):
    ```bash
    python -m venv venv
    # On Windows:
    venv\Scripts\activate
    # On macOS/Linux:
    source venv/bin/activate
    ```

3.  **Install the required dependencies:**
    ```bash
    pip install streamlit pandas networkx folium streamlit-folium matplotlib
    ```

4.  **Run the Streamlit app:**
    ```bash
    streamlit run main.py
    ```

5.  **Access the application:** Open your browser and navigate to the local URL provided in the terminal (usually `http://localhost:8501`).

## 🖥️ How to Use

Once the app is running, use the **Sidebar Navigation** to switch between different modules:
*   **Home:** Overview of the platform.
*   **Road Network View:** Explore the geospatial map of Cairo.
*   **MST Road Network:** View the theoretical Minimum Spanning Tree overlay.
*   **Traffic Flow Optimization:** Select origin/destination and time of day to find the best driving route.
*   **Emergency Routing:** Select an origin to simulate an emergency vehicle routing to the nearest hospital.
*   **Public Transit Optimization:** Find multi-modal transit routes.

## 🏙️ Impact

This project aims to assist urban planners and decision-makers in:
*   **Reducing congestion** and commuting travel times.
*   **Improving public transit accessibility** and integration.
*   **Supporting emergency services** with dynamic, traffic-aware routing.
*   **Optimizing budget allocation** for new road constructions based on MST models.

---

## Author

Tasneem Ibrahim - Rokaia Islam - Hazem Orbay - Abulrahman Ibrahim - Wafaa Mohamed
