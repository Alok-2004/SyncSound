# 🎵 SyncSound

**SyncSound** is a real-time video synchronization app that allows multiple users to watch YouTube videos together in perfect sync. It follows a **master-slave architecture**, where the **Master** controls playback and synchronization, and **Clients** receive signals to stay in sync.

Built with:
- ⚙️ Node.js + Express + Web Sockets (Backend)
- ⚛️ React.js (Frontend)
- 📺 YouTube iFrame API (for video playback)
- 💻 WebSocket-based communication

---

## 🚀 Features

- 🎬 Master-controlled video playback
- 🔄 Real-time synchronization across multiple clients
- 👥 Dynamic role assignment (any client can become Master)
- 🛰 Graceful handling of signal loss or disconnection
- 📡 Status dashboard for connected clients
- 🔄 Re-sync feature to realign lagging clients

---

## 🛠 Tech Stack

| Layer       | Tech                       |
|------------|-----------------------------|
| Frontend   | React, Tailwind CSS         |
| Backend    | Node.js, Express, Socket.IO |
| Video API  | YouTube IFrame API          |
| Syncing    | WebSockets                  |

---


## ⚙️ Backend Development Phases

We’re actively working through a series of backend milestones to bring SyncSound to full functionality:

### ✅ Phase 1: Sync/Resync System (🎯 _Current Phase_)
- Implement WebSocket connection for real-time control
- Master emits `play`, `pause`, and `seek` events
- Clients receive and sync playback state accordingly
- Automatic recovery for lagging clients

### 🔜 Phase 2: Upgrade Slave to Master
- Any client can be promoted to master upon disconnection or manually
- Handle master reassignment across rooms
- Promote with `promoteToMaster` event

### 🔜 Phase 3: Room Management
- Create and join virtual rooms
- Manage multiple sync sessions independently
- Rooms identified by unique codes

### 🔜 Phase 4: Session-Based Authentication
- Login system with JWT + cookies
- User profiles and persistent identity
- Access control for private/public rooms

### 🔜 Phase 5: Deployment
- cloud(most Probably AWS) + CI/CD

### 🔜 Phase 6: Chat + Friends System
- Real-time room-based chat
- Friend list and private invites
- Online status visibility

---