# 🚀 Smart Route Optimization System

A full-stack GIS-based route optimization system that computes optimized routes across Cairo using real road-network data from OpenStreetMap.

The application combines graph algorithms, interactive maps, and modern web technologies to provide route optimization, navigation, and route management similar to a lightweight GPS application.

---

## ✨ Features

### 🗺️ Route Planning
- Select a start location and multiple destinations
- Optimize routes using either:
  - Greedy Algorithm (fast heuristic)
  - Traveling Salesman Problem (TSP) approximation
- Interactive map visualization
- Animated route rendering
- Turn-by-turn directions
- Total distance and estimated travel time (ETA)

### 📍 Navigation
- Live GPS location tracking
- Automatic map updates
- Road geometry generated using OSRM
- Real-world routing over Cairo's road network

### ⭐ User Features
- JWT Authentication
- Save favorite locations
- Route history
- Restore previous routes
- Search locations using OpenStreetMap

### ⚡ Performance
- In-memory shortest-path cache
- MongoDB routing cache
- MongoDB geo cache
- Asynchronous history saving
- Cached road network graph

---

# 🏗️ Tech Stack

## Frontend

- React
- Leaflet
- Fetch API

## Backend

- Python
- Django
- Django REST Framework

## Database

- MongoDB
- SQLite

## GIS & Routing

- OpenStreetMap
- OSMnx
- NetworkX
- OSRM

---

# 🧠 Algorithms

## Greedy Algorithm

Visits the nearest destination first.

✔ Fast

✔ Good for many locations

❌ Doesn't always produce the shortest overall route.

---

## Traveling Salesman Problem (TSP)

Computes a near-optimal order for visiting all destinations before constructing the final route.

✔ Better overall routes

✔ Optimized total travel distance

---

# 📡 API Endpoints

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | `/routes/optimize-route/` | Compute optimized route |
| GET | `/routes/history/` | Retrieve user route history |
| GET | `/routes/location_path/<id>/` | Retrieve saved route path |
| GET | `/routes/search-location/` | Search locations |
| GET | `/routes/favorites/` | Retrieve favorites |
| POST | `/routes/favorites/add/` | Save favorite |
| POST | `/routes/favorites/remove/` | Remove favorite |
| POST | `/api/token/` | Login |
| POST | `/api/token/refresh/` | Refresh JWT |

---

# 🖥️ Project Architecture

```text
                React + Leaflet
                       │
                  REST API
                       │
          Django REST Framework
                       │
      ┌───────────┬────────────┐
      │           │            │
   MongoDB     SQLite      JWT Auth
      │
 Route History
 Favorites
 Routing Cache
 Geo Cache
      │
 OpenStreetMap
      │
    OSMnx
      │
   NetworkX
      │
 Route Optimization
      │
     OSRM
      │
Geometry • ETA • Directions
```

---


## 📸 Demo

![alt text](image.png)

- Interactive Map
- Route Optimization
- Route History
- Favorites
- Live Tracking

---

# ⚙️ Installation

## Backend

```bash
cd backend

python -m venv venv

source venv/bin/activate      # Linux/macOS
venv\Scripts\activate         # Windows

pip install -r requirements.txt

python manage.py migrate

python manage.py runserver
```

---

## Frontend

```bash
cd frontend

npm install

npm run dev
```

---

# 🚀 Future Improvements

- 🚦 Traffic visualization with segmented colored roads
- 🛣️ Alternative route suggestions
- 🐳 Docker support
- ☁️ Cloud deployment
- 🎙️ Voice search
- 📱 Mobile-responsive UI
- 🔔 Voice navigation
- 🚗 Real-time traffic-aware routing

---

# 👨‍💻 Author

**Rania Raafat**

Backend Software Engineer

LinkedIn: https://linkedin.com/in/rania-raafat-694b0b261
