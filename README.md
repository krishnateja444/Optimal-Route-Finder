# 🚆 Rail Yatra – Optimal Railway Path Finder

An interactive railway route planning application built with **Python**, **Streamlit**, **Graphs**, and **Dijkstra's Algorithm** to find the shortest route between railway stations.

---

## 📌 Overview

Rail Yatra models a railway network as a weighted graph where:

* Stations represent graph vertices.
* Railway connections represent weighted edges.
* Distances between stations are edge weights.

The application uses **Dijkstra's Shortest Path Algorithm** with a **Min Heap (Priority Queue)** to efficiently compute the shortest route and total travel distance between any two stations.

---

## ✨ Features

* 🚉 Railway network modeled using Graph Data Structure
* ⚡ Fast shortest-path computation using Dijkstra's Algorithm
* 🖥️ Interactive Streamlit web interface
* 📏 Displays total route distance
* 🛤️ Shows complete station-by-station path
* 🔄 Supports bidirectional railway connections
* 📚 Demonstrates practical application of Graphs and Heaps

---

## 🛠️ Technologies Used

* Python
* Streamlit
* Graph Data Structure
* Dijkstra's Algorithm
* Heap Queue (`heapq`)

---

## 📂 Project Structure

```text
Optimal_Railway_Path_Finder/
│
├── optimal_path_finder.py
├── README.md
└── requirements.txt
```

---

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Optimal_Railway_Path_Finder.git
cd Optimal_Railway_Path_Finder
```

### 2. Install Dependencies

```bash
pip install streamlit
```

### 3. Run the Application

```bash
streamlit run optimal_path_finder.py
```

---

## 🎯 How It Works

1. Select a source station.
2. Select a destination station.
3. Click **Find Route**.
4. The application computes:

   * Shortest route
   * Total distance
5. Results are displayed instantly.

---

## 🧠 Algorithm

### Dijkstra's Shortest Path Algorithm

The algorithm maintains the shortest known distance from the source station to every other station and continuously expands the nearest unvisited station using a priority queue.

**Time Complexity**

```text
O((V + E) log V)
```

**Space Complexity**

```text
O(V)
```

Where:

* V = Number of Stations
* E = Number of Railway Connections

---

## 💻 Example

```python
railway = RailwayPlanner()

railway.add_station("Hyderabad")
railway.add_station("Vijayawada")

railway.add_connection(
    "Hyderabad",
    "Vijayawada",
    299
)

path, distance = railway.shortest_path(
    "Hyderabad",
    "Vijayawada"
)

print(path)
print(distance)
```

Output:

```text
['Hyderabad', 'Vijayawada']
299
```

---

## 🔮 Future Enhancements

* Add more railway stations and routes
* Route visualization using NetworkX
* Interactive railway map
* Alternative route suggestions
* Estimated travel time calculation
* Fare estimation
* Real-time train schedule integration


## ⚠️ Disclaimer

This project is created for educational and learning purposes. Route information is based on a simplified railway network and should not be used for actual travel planning.
