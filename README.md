# ⛽ RoadAssist — On-Road Fuel & Breakdown Assistance System

AI-powered, real-time roadside assistance platform for fuel delivery, towing, mechanics, and emergency SOS — built for Indian highways.

---

## ✨ Features

| Category | Feature |
| :--- | :--- |
| 🆘 **Emergency** | SOS button, multi-step request form, instant dispatch |
| 🗺️ **Map** | Live provider tracking, route optimization, interactive map view |
| 🤖 **ML** | Breakdown risk prediction, smart provider recommendation, fuel demand forecasting |
| ⚡ **Real-Time** | Socket.IO live location updates, push notifications, status tracking |
| 🔐 **Auth** | JWT authentication, role-based access (`user` / `provider` / `admin`) |
| 🌙 **UI** | Dark / Light mode toggle, fully responsive modern layout |
| 👑 **Admin** | Central dashboard, live request feed, provider verification workflow |

---

## 🛠 Tech Stack

- **Frontend:** HTML5, CSS3, Vanilla JavaScript, Maps API
- **Backend:** Node.js, Express.js, Socket.IO
- **Database:** SQLite (default / zero-config) or MySQL via Sequelize ORM
- **ML Service:** Python, FastAPI, scikit-learn
- **Authentication:** JWT, bcryptjs

---

## 🚀 Quick Start (Local Setup)

### 1. Backend
```bash
cd backend
npm install
npm run dev
```
Runs on `http://localhost:5001`. SQLite database (`roadassist.sqlite`) is initialized automatically.

---

### 2. Machine Learning Service
```bash
cd ml-service
pip install -r requirements.txt
python train_models.py
uvicorn main:app --reload --port 8000
```
Runs on `http://localhost:8000`. Access interactive API documentation at `http://localhost:8000/docs`.

---

### 3. Frontend
```bash
cd frontend
npx live-server --port=3000
```
Open `http://localhost:3000/pages/index.html` in your browser.

---

## 📸 Pages

| Page | Path | Description |
| :--- | :--- | :--- |
| **Home Dashboard** | `/pages/index.html` | Services overview, live activity feed, AI insights |
| **Emergency Request** | `/pages/emergency.html` | 3-step assistance request form, interactive map, provider details |
| **Live Map** | `/pages/map.html` | Real-time provider locations and active service tracking |
| **Profile** | `/pages/profile.html` | User authentication, request history, user preferences |
| **Admin Panel** | `/pages/admin.html` | System analytics, incident management, provider verification |

---

## 📡 ML Models

- **Breakdown Risk Predictor:** `RandomForestClassifier` trained on road geometry, traffic density, and weather conditions → classifies risk into **Low**, **Medium**, **High**, or **Critical**.
- **Fuel Demand Forecaster:** `GradientBoostingRegressor` → outputs an area-wise demand score scaled from **0 to 100**.
- **Provider Recommender:** Weighted scoring algorithm:
  $$\text{Score} = (0.50 \times \text{Distance}) + (0.30 \times \text{Rating}) + (0.20 \times \text{Experience})$$

---

## 📄 License

Distributed under the MIT License. Built for educational
