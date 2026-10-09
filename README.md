# Cairo Transport Optimization System 🚀

Welcome to the **Cairo Transport Optimization System**, a smart planning and analysis tool built with Streamlit. This application is designed to model, analyze, and improve the public and private transportation networks across Greater Cairo using graph theory algorithms, network analysis, and interactive mapping.

## Features 🌟

*   **🛣️ Road Network Visualization:** Interactive map visualizing the current and proposed road networks.
*   **🌉 MST Road Network:** Computes and visualizes the Minimum Spanning Tree (MST) for the road network using Kruskal's algorithm to optimize construction costs and distance.
*   **🚦 Traffic Flow Optimization:** Identifies the most efficient driving routes using Dijkstra's algorithm based on real-time traffic conditions across different time periods (Morning, Afternoon, Evening, Night). Includes congestion analysis and alternate route suggestions.
*   **🚑 Emergency Routing:** Employs the A* search algorithm to compute the fastest response paths for emergency services to reach hospitals, factoring in traffic conditions and traffic signal preemption.
*   **🚍 Public Transit Optimization:** Utilizes Dynamic Programming to suggest optimal routes using multiple transit modes (Bus, Metro, Walking), minimizing travel time and transfer penalties.

## Tech Stack 🛠️

*   **Python:** Core programming language.
*   **Streamlit:** Web application framework for the interactive user interface.
*   **Pandas:** Data manipulation and analysis of CSV datasets.
*   **NetworkX:** Graph modeling and analysis algorithms (Dijkstra, A*, MST/Kruskal).
*   **Folium & Streamlit-Folium:** Interactive map generation and visualization.
*   **Matplotlib:** Plotting graphs and network visualizations.

## Project Structure 📁

*   `main.py`: The main Streamlit application script containing all the pages, logic, and UI components.
*   `Read.py`: Auxiliary script for data reading and processing.
*   `*.csv`: Various datasets containing information about neighborhoods, roads, traffic flow, facilities, bus routes, metro lines, and transport demand.
*   `cairo_traffic_map.html`: Pre-generated traffic map visualization.

## How to Run 🏃‍♂️

1.  **Ensure you have Python installed.**
2.  **Install the required dependencies:**
    ```bash
    pip install streamlit pandas networkx folium streamlit-folium matplotlib
    ```
3.  **Run the Streamlit app:**
    ```bash
    streamlit run main.py
    ```
4.  **Open your browser** to the local URL provided in the terminal (usually `http://localhost:8501`).

## Data 📊

The system relies on various datasets representing Cairo's infrastructure:
*   **Areas & Neighborhoods:** Demographics and coordinates.
*   **Roads:** Existing and planned road networks with distances and costs.
*   **Traffic:** Volume data across different times of the day.
*   **Facilities:** Locations of key facilities like hospitals.
*   **Public Transit:** Bus routes and Metro lines with frequencies.

## Impact 🏙️

This project aims to assist urban planners and decision-makers in:
*   Reducing congestion and travel times.
*   Improving public transit accessibility.
*   Supporting emergency services with dynamic routing.
