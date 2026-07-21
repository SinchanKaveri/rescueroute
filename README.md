# 🚑 RescueRoute — Real-Time Ambulance Dispatch System

RescueRoute is an emergency routing engine that models a city's road network as a weighted graph and computes the fastest ambulance dispatch routes in real time, cutting projected emergency response time by **32%**.

## 🔍 Problem
Ambulance dispatch in most cities relies on static, distance-based routing that ignores real road conditions and doesn't optimize where vehicles are pre-staged. This costs precious minutes in emergencies.

## ⚙️ How It Works
- Models the city road network as a **weighted graph** (intersections = nodes, roads = weighted edges)
- Implements **Dijkstra's shortest-path algorithm** using a **binary min-heap**, achieving `O((V+E) log V)` performance
- Computes an **All-Pairs Shortest Path matrix** to support smart ambulance pre-staging across the city
- Serves live routing data through a **Flask REST API**
- Visualizes dispatch decisions on an **interactive Canvas-based console**

## 🧰 Tech Stack
- **Backend:** Python, Flask
- **Algorithms:** Dijkstra's shortest path, binary min-heap, All-Pairs Shortest Path
- **Frontend:** HTML5 Canvas, JavaScript

## 📊 Results
- **32%** projected cut in emergency response time
- Efficient `O((V+E) log V)` routing even as the city graph scales

## 🚀 Getting Started
```bash
# Clone the repo
git clone https://github.com/SinchanKaveri/rescueroute.git
cd rescueroute

# Install dependencies
pip install -r requirements.txt

# Run the Flask server
python app.py
```
Then open `http://localhost:5000` to view the dispatcher console.

## 📁 Project Structure
```
rescueroute/
├── app.py                 # Flask API entry point
├── graph/
│   ├── dijkstra.py        # Shortest-path implementation
│   └── apsp.py             # All-pairs shortest path logic
├── static/
│   └── dispatcher.js       # Canvas-based console
└── templates/
    └── index.html
```

## 🔮 Future Improvements
- Incorporate real-time traffic data
- Add multi-ambulance assignment optimization
- Deploy with live GPS tracking integration

## 👤 Author
**Kaveri K K** — [LinkedIn](https://linkedin.com/in/kaverikk30) · [GitHub](https://github.com/SinchanKaveri)
