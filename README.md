<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=wave&color=0ea5e9&height=200&section=header&text=INSIGHTDRIVE&fontSize=70&fontAlignY=35" />

  <h2>🌟 Real-time Ride Feedback Intelligence for Safer Fleet Operations</h2>

  <p align="center">
    <a href="#overview">Overview</a> •
    <a href="#features">Features</a> •
    <a href="#tech-stack">Tech Stack</a> •
    <a href="#getting-started">Getting Started</a>
  </p>

  <p align="center">
    <img alt="last-commit" src="https://img.shields.io/github/last-commit/Retik29/InsightDrive?style=for-the-badge&logo=git&logoColor=white&color=0ea5e9">
    <img alt="repo-top-language" src="https://img.shields.io/github/languages/top/Retik29/InsightDrive?style=for-the-badge&color=0ea5e9">
    <img alt="repo-language-count" src="https://img.shields.io/github/languages/count/Retik29/InsightDrive?style=for-the-badge&color=0ea5e9">
  </p>

  <h3>🚀 Built with the Power of MERN 🚀</h3>

  <p align="center">
    <img alt="MongoDB" src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white">
    <img alt="Express" src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white">
    <img alt="React" src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black">
    <img alt="Node.js" src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white">
  </p>
  <p align="center">
    <img alt="Mongoose" src="https://img.shields.io/badge/Mongoose-F04D35?style=for-the-badge&logo=mongoose&logoColor=white">
    <img alt="Socket.IO" src="https://img.shields.io/badge/Socket.IO-010101?style=for-the-badge&logo=socketdotio&logoColor=white">
    <img alt="Vite" src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white">
    <img alt="Tailwind" src="https://img.shields.io/badge/TailwindCSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white">
  </p>
</div>

<hr />

## 📖 <span id="overview">Overview</span>

**InsightDrive** is not just another feedback platform; it’s an **intelligent, full-stack fleet feedback ecosystem** engineered for proactive transportation teams! 🚗💨

By seamlessly bridging the gap between commuters and operations admins, InsightDrive ensures that every ride is monitored for quality and safety. Users can easily submit structured trip feedback, whilst admins keep their eyes on the road using a live, real-time analytics dashboard loaded with leaderboard views and instant incident alerts.

---

## ✨ <span id="features">Key Features</span>

- 🔐 **Role-Based Mastery:** Secure JWT-based cookie authentication separating users from powerful admins.
- 🛣️ **Frictionless Trip Workflows:** Let users generate sample rides and effortlessly submit detailed ride + driver feedback.
- ⭐ **App Rating Engine:** A dedicated `Rate App` portal, allowing users to constantly update their platform experience.
- 🧠 **Smart Driver Intelligence:** Automated calculation of average ratings and feedback tallies, creating a fair, data-driven driver profile.
- 📊 **Stunning Admin Analytics:** Dive deep into sentiment algorithms and trends through dynamic, interactive charts using 30-day historical data.
- 🏆 **Dynamic Leaderboards & Audit Trails:** Track top performers with paginated lists and scrub through a complete feedback log with surgical sorting/filtering.
- 🚨 **Realtime Incident Alerts:** Utilizing WebSocket magic (Socket.IO) to push live, immediate notifications for low-score ratings directly to the admin terminal.

---

## 🛠️ <span id="tech-stack">Technical Architecture & Stack</span>

At its core, **InsightDrive** boasts a clean, modular MERN architecture that screams performance and scalability.

### **The Stack**
- **Frontend 🎨:** React 19, React Router, Vite, Tailwind CSS, Recharts, Axios, React Toastify, Socket.IO Client.
- **Backend ⚙️:** Node.js, Express, Mongoose, JWT, Cookie Parser, CORS, Socket.IO.
- **Database 🗄️:** MongoDB (Local or Atlas compatible).

### **The Architecture**
- 🖼️ **Presentation Layer (Client):** Fast route-based pages, reactive UI components, robust API abstraction, and beautiful toast notifications.
- 🔌 **API Layer (Server):** Highly organized RESTful routes mapping directly to rich domain logic (`auth`, `rides`, `feedback`, `app-feedback`, `drivers`).
- ⚡ **Realtime Layer:** Instant event-driven WebSocket emitting (`low-score-alert`) for immediate crisis management.

---

## 🚀 <span id="getting-started">Getting Started (Local Supremacy)</span>

Ready to harness InsightDrive on your local machine? Let's get things rolling!

### 📋 Prerequisites
- **Node.js:** v18+ Recommended.
- **MongoDB:** Locally installed and running.

### ⚙️ Installation & Setup

1️⃣ **Environment Setup:**
We've streamlined the local `.env` setup. Check your `client` and `server` folders, they are pre-configured locally now!

**`server/.env` example:**
```env
PORT=5000
MONGO_URI=mongodb://127.0.0.1:27017/insightdrive
JWT_SECRET=super_secret_jwt_key_for_insightdrive_local
JWT_EXPIRES_IN=1d
NODE_ENV=development
CLIENT_URL=http://localhost:5173

# Reserved Admin Arsenal
ADMIN_NAME=Admin
ADMIN_EMAIL=admin@gmail.com
ADMIN_PASSWORD=123456
```

**`client/.env` example:**
```env
VITE_API_BASE_URL=http://localhost:5000/api
VITE_SOCKET_URL=http://localhost:5000
```

2️⃣ **Dependency Installation:**
```bash
# Terminal 1 - Fuel the Backend
cd server
npm install
npm run dev

# Terminal 2 - Ignite the Frontend
cd client
npm install
npm run dev
```

**Boom! 💥 You're live.**
- 🌐 Client App: `http://localhost:5173`
- 🖥️ Server API: `http://localhost:5000`

---

## 📡 API Endpoints Arsenal

A sneak peek into the backend engine driving InsightDrive:

| Module | Method | Endpoint | Access |
|---|---|---|---|
| **Health** | `GET` | `/health` | Public |
| **Auth** | `POST` | `/auth/register` \| `/auth/login` \| `/auth/logout` | Public |
| **Auth** | `GET` | `/auth/me` | Protected |
| **Rides** | `POST` | `/rides/generate` | User |
| **Feedback** | `POST` | `/feedback` | User |
| **Feedback**| `GET` | `/feedback/all` \| `/feedback/analytics` | Admin |
| **Drivers** | `GET` | `/drivers` | Protected |

> Explore more dynamically within the app!

---

## 🛡️ Authentication & Roles

Security is non-negotiable. InsightDrive uses industry-standard JWT stored securely in HTTP-only cookies.
1. **Users** generate rides and provide essential feedback.
2. **Admins** hold the keys. Login securely using the `ADMIN_EMAIL` and `ADMIN_PASSWORD` defined in your `.env`.

---

## 🔮 Future Horizons

We're constantly evolving! Here's what's brewing:
- 🤖 Automated test suites (Unit, Integration, API contracts).
- 🔄 Enhanced refresh tokens & Session management.
- 🛡️ Advanced API rate limiting.
- 🚀 Modern CI/CD deployment workflows.

---

<div align="center">
  <h3>Ready to take the wheel?</h3>
  <p>Star ⭐ this repository and start building better fleet experiences with InsightDrive!</p>
  <img src="https://capsule-render.vercel.app/api?type=wave&color=0ea5e9&height=100&section=footer" />
</div>
