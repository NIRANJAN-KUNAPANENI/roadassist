# ⛽ RoadAssist — On-Road Fuel & Breakdown Assistance System

> AI-powered, real-time roadside assistance platform for fuel delivery, towing, mechanics, and emergency SOS — built for Indian highways.

---

## ✨ Features

| Category | Feature |
| :--- | :--- |
| 🆘 **Emergency** | SOS button, multi-step request form, instant dispatch |
| 🗺️ **Map** | Live provider tracking, route optimization, interactive map view |
| 🤖 **ML** | Breakdown risk prediction, smart provider recommendation, fuel demand forecasting |
| ⚡ **Real-Time** | Socket.IO live location updates, push notifications, status tracking |
| 🔐 **Auth** | JWT authentication, role-based access (user/provider/admin) |
| 🌙 **UI** | Dark/Light mode, fully responsive layout |
| 👑 **Admin** | Dashboard, request management, provider verification |

---

## 🛠 Tech Stack

- **Frontend:** HTML5, CSS3, Vanilla JavaScript, Maps API
- **Backend:** Node.js, Express.js, Socket.IO
- **Database:** SQLite (default / zero-config) or MySQL via Sequelize ORM
- **ML Service:** Python, FastAPI, scikit-learn
- **Auth:** JWT, bcryptjs

---

## 🚀 Quick Start (Local Setup)

### 1. Backend
```bash
cd backend
npm install
npm run dev
Runs on http://localhost:5001. SQLite database (roadassist.sqlite) is initialized automatically.

2. Machine Learning Service
Bash
cd ml-service
pip install -r requirements.txt
python train_models.py
uvicorn main:app --reload --port 8000
Runs on http://localhost:8000. View interactive docs at http://localhost:8000/docs.

3. Frontend
Bash
cd frontend
npx live-server --port=3000
Open http://localhost:3000/pages/index.html in your browser.

📸 Pages
Page	Path	Description
Home Dashboard	/pages/index.html	Services overview, live feed, AI insights
Emergency Request	/pages/emergency.html	3-step assistance form, map, provider card
Live Map	/pages/map.html	Real-time provider map & active tracking
Profile	/pages/profile.html	User auth, request history, settings
Admin	/pages/admin.html	System analytics, provider verification
📡 ML Models
Breakdown Risk Predictor: RandomForestClassifier trained on road and weather conditions → classifies risk into Low, Medium, High, or Critical.

Fuel Demand Forecaster: GradientBoostingRegressor → outputs a 0–100 demand score.

Provider Recommender: Weighted scoring algorithm (Distance 50% + Rating 30% + Experience 20%).

📄 License
MIT — Built for educational and portfolio purposes.
'@ | Set-Content -Path "README.md" -Encoding UTF8

git add README.md backend/.gitignore
git commit -m "docs: update and clean up project documentation"
git push origin main
