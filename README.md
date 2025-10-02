# Real-Time Collaborative Text Editor (with MongoDB)

A complete full-stack project that provides a **real-time collaborative text editor**, similar to Google Docs. 
It is built using **React.js, Node.js, Express, Socket.IO, and MongoDB**. 
The project highlights real-time editing features, **persistent data storage with MongoDB**, and is designed for students and developers who want to explore full-stack development.

## 🚀 Quick Start

### Requirements
- **Node.js** (v16+) → [Download](https://nodejs.org/)
- **MongoDB** → [Setup Guide](#-mongodb-setup)
- **npm** (bundled with Node.js)

### Installation Steps

1. **Extract the repository**
   ```bash
   cd collaborative-text-editor-mongodb
   ```

2. **Configure MongoDB**  
   - Install and run MongoDB locally  
   - Default URI: `mongodb://localhost:27017`

3. **Run Backend**
   ```bash
   cd backend
   npm install
   cp .env.example .env   # configure if necessary
   npm start
   ```
   Runs on → http://localhost:5000

4. **Run Frontend (new terminal)**
   ```bash
   cd frontend
   npm install
   npm start
   ```
   Runs on → http://localhost:3000

### Test Collaboration
- Open multiple tabs at http://localhost:3000  
- Use different usernames, same document ID (try `demo-doc`)  
- Type in one tab → changes appear in others instantly  
- Refresh page → content persists in MongoDB  

## 🗄️ MongoDB Setup (Local)
- Download from: https://www.mongodb.com/try/download/community  
- Install and follow setup wizard  
- Service runs automatically at: `mongodb://localhost:27017`

## 🎯 Core Features

- **Real-Time Editing** → Multi-user text sync, typing indicators, user presence  
- **MongoDB Persistence** → Documents auto-save, survive restarts, track versions  
- **Rich Text Tools** → Bold, italic, underline, lists, colors, shortcuts  
- **Document Management** → Create/join by ID, share via URL, demo-doc included  
- **User Experience** → Avatars, last-saved status, responsive design, clean UI  

## 🏗️ Project Structure
```
collaborative-text-editor-mongodb/
├── backend/   → Node.js + Express + Socket.IO + MongoDB
├── frontend/  → React.js client with editor, user list, toolbar
└── README.md
```

## 🔧 Tech Stack
- **Backend**: Node.js, Express, Socket.IO, MongoDB, Mongoose, dotenv, CORS  
- **Frontend**: React.js, Socket.IO Client, HTML5 ContentEditable, CSS  

## 📊 MongoDB Schema
```json
{
  "documentId": "string",
  "title": "string",
  "content": "string",
  "lastModified": "date",
  "collaborators": [
    {"username": "string", "color": "string", "joinedAt": "date"}
  ]
}
```

## 📚 Learning Goals
- WebSockets & event-driven programming  
- MongoDB + Mongoose integration  
- React state, hooks, and component communication  
- Full-stack real-time applications  

## 🚀 API Routes
- `GET /api/documents/:id` → Fetch document  
- `POST /api/documents` → Create document  
- `PUT /api/documents/:id` → Update document  
- `GET /api/documents` → List documents  

## 🔌 Socket.IO Events
- **Client → Server**: `join-document`, `leave-document`, `text-change`, `title-change`, `cursor-position`, `user-typing`  
- **Server → Client**: `document-loaded`, `text-updated`, `user-joined`, `user-left`, `typing-indicator`  

## 🛠️ Future Improvements
- Authentication + access control  
- Document history + comments  
- Export/import (PDF/Word)  
- Redis caching & scaling with MongoDB Atlas  

## 🔐 Environment Variables
```bash
MONGODB_URI=mongodb://localhost:27017/collaborative-editor
PORT=5000
NODE_ENV=development
FRONTEND_URL=http://localhost:3000
```

## 👨‍💻 Contribution
Ideal for:
- CS students learning full-stack development  
- Developers exploring MongoDB + WebSockets  
- Anyone building collaborative editing apps  

## 📝 Screenshots 



---
✨ Built with passion for full-stack learning ✨
