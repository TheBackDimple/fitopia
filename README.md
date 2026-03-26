# 💪 Fitopia

A gamified fitness web app built to make working out feel like a game. 
Users complete quests, earn achievements, climb leaderboards, and get 
personalized guidance through an integrated AI assistant — all backed 
by a persistent MongoDB Atlas database.

Built as a full-stack group project at UCF.

---

## 🧱 System Architecture
```
React + Vite Frontend → Express REST API → MongoDB Atlas
                     ↘ AI Chat Assistant
```

| Layer | Technology |
|---|---|
| Frontend | React · TypeScript · Vite |
| Backend | Node.js · Express.js |
| Database | MongoDB Atlas |
| Auth | JWT · Security Questions |
| AI Assistant | Chat integration |
| 3D Assets | GLB models (Three.js) |

---

## ⚙️ Features

- JWT-based auth with registration, login, and forgot password flow
- Daily quests and gym quests with completion tracking
- Weekly routine system with persistent progress
- Leaderboard with real-time user rankings
- Achievements system (daily, monthly, lifetime)
- AI chat assistant for fitness guidance
- 3D animated UI elements
- Settings and profile management

---

## 📁 Project Structure
```
fitopia/
├── backend/
│   ├── server.js           # Express entry point
│   ├── config/
│   │   └── db.js           # MongoDB Atlas connection
│   ├── controllers/
│   │   └── authController.js
│   ├── models/
│   │   ├── User.js
│   │   ├── Workout.js
│   │   ├── Quest.js
│   │   └── WeeklyRoutine.js
│   └── routes/
│       ├── authRoutes.js
│       └── routineRoutes.js
└── frontend/
    └── src/
        ├── components/     # Reusable UI components
        ├── pages/          # Route-level page components
        ├── data/           # Static data (security questions)
        └── styles/         # CSS modules and theme
```

---

## 📊 Database

MongoDB Atlas with 5 collections:

| Collection | Purpose |
|---|---|
| Users | Auth, profiles, progression |
| Workouts | Workout logging |
| Quests | Daily and gym quest tracking |
| WeeklyRoutines | Weekly routine persistence |
| Achievements | Daily, monthly, lifetime records |

---

## 📈 Metrics

| | |
|---|---|
| Registered users | 31 |
| Active quests | 35 |
| Weekly routines | 17 |
| Collections | 5 |
| Auth endpoints | Registration · Login · Forgot Password |

---

## 🚀 Getting Started
```bash
# Clone the repo
git clone https://github.com/TheBackDimple/fitopia.git
cd fitopia

# Install root dependencies
npm install

# Start backend
cd backend
npm install
node server.js

# Start frontend (new terminal)
cd frontend
npm install
npm run dev
```

Make sure to add a `.env` file in `/backend` with your MongoDB 
Atlas connection string:
```
MONGO_URI=your_mongodb_atlas_connection_string
JWT_SECRET=your_jwt_secret
```

---

## 👤 Author

**Abdiel Marcano** — [Portfolio](https://abdielMarcano.dev) · 
[LinkedIn](https://linkedin.com/in/abdiel-marcano)
