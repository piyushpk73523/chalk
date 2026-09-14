# **🖊️ Chalk – Real-Time Collaborative Whiteboard**

Chalk is a real-time collaborative whiteboard app where users can draw, write, and brainstorm together in a shared space — all powered by **WebSockets, Redis, and PostgreSQL**.

Built with **Next.js**, **Node.js**, **WebSockets**, **Redis**, **PostgreSQL**, and **Prisma**, Chalk delivers a fast and seamless real-time canvas experience.

---

## **🌐 Live Demo**

🚀 **[Try Chalk Live](https://chalk-frontend-red.vercel.app/)**

---

## **🚀 Features**

- 🎨 Real-time collaborative drawing
- 🧠 Multi-user whiteboard rooms
- 🖼️ Excalidraw-style canvas
- 💾 Persistent application data using PostgreSQL
- 🔴 Redis-powered real-time infrastructure
- 🔒 Room-based architecture
- ⚡ Real-time communication using WebSockets
- 🔐 JWT-based authentication
- 💬 Room-based chat functionality
- 🟢 Online user tracking

---

## **🛠️ Tech Stack**

- **Frontend:** Next.js, React, TypeScript, Tailwind CSS
- **Backend:** Node.js, Express.js, TypeScript
- **Real-Time:** WebSockets, Redis, BullMQ
- **Database:** PostgreSQL, Prisma ORM
- **Deployment:** Vercel, Render, Neon, Upstash
- **Package Manager:** pnpm
- **Monorepo:** Turborepo

---

## **🛠️ Getting Started**

Follow these steps to run the project locally:

### **1. Clone the repository**

```bash
git clone https://github.com/piyushpk73523/chalk.git

cd chalk
2. Install dependencies
pnpm install
3. Set up PostgreSQL

You can use either:

Option A: Local PostgreSQL

Update your .env file with the connection string:

DATABASE_URL=postgresql://postgres:yourpassword@localhost:5432/chalk

Option B: Neon PostgreSQL

Create a database using Neon and copy the connection string:

DATABASE_URL=your_neon_database_url
4. Set up Redis (Required)

For local development, you can use Docker:

docker run --name redis_server -p 6379:6379 -d redis

Then configure:

REDIS_URL=redis://localhost:6379

You can also use a cloud Redis provider such as Upstash.

5. Configure JWT

Add your JWT secret to your environment variables:

JWT_SECRET=your_jwt_secret

Note: Never commit your .env file or production secrets to GitHub.

6. Generate Prisma Client
pnpm db:generate
7. Run database migrations
npx prisma migrate deploy
8. Run the development server
pnpm run dev
Your app should now be running at http://localhost:3000
☁️ Production Deployment

Chalk is deployed using separate services:

Frontend: Vercel
Backend: Render
WebSocket Server: Render
Database: Neon PostgreSQL
Redis: Upstash
Production URLs

Frontend:
https://chalk-frontend-red.vercel.app/

Backend:
https://chalk-backend-fgw2.onrender.com

WebSocket:
https://chalk-websocket.onrender.com

## 📸 Screenshots

### 🏠 Home Page

![Home Page](./assets/home.png)

---

### ✏️ Drawing Room

![Drawing Room](./assets/drawing-room.png)

---

### 🔄 Real-time Dashboard (GIF)

![Real-time Collab](./assets/dashboard.png)


🏗️ Project Structure
chalk/
│
├── apps/
│   ├── chalk-frontend/       # Next.js frontend
│   ├── chalk-http/           # Express backend
│   └── chalk-websocket/      # WebSocket server
│
├── packages/
│   ├── db/                   # Prisma & PostgreSQL
│   ├── redis/                # Redis configuration
│   └── common/               # Shared utilities
│
├── package.json
├── pnpm-lock.yaml
├── pnpm-workspace.yaml
└── turbo.json
🔄 Real-Time Collaboration

Chalk uses WebSockets and Redis to synchronize whiteboard updates between multiple connected users.

User A
   ↓
Next.js Frontend
   ↓
WebSocket Server
   ↓
Redis
   ↓
Connected Users
   ↓
Real-Time Whiteboard Updates

Open the same room in multiple browser windows to experience real-time collaboration.

👨‍💻 Author

Piyush Kumar

Full Stack Developer | B.Tech – Information Technology

GitHub: @piyushpk73523
LinkedIn: Piyush Kumar
⭐ Support

If you like this project, please consider giving the repository a ⭐ on GitHub.

Built with ❤️ using Next.js, Node.js, WebSockets, Redis & PostgreSQL.