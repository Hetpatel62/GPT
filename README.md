# SigmaGPT 🤖

A full-stack ChatGPT replica built from scratch using the MERN stack and OpenAI API. SigmaGPT supports persistent chat threads, multi-turn conversations, and a clean React-based UI.

---

## 🛠 Tech Stack

**Frontend**
- React 19 + Vite
- React Markdown + Rehype Highlight (code block rendering)
- React Spinners
- UUID (thread ID generation)

**Backend**
- Node.js + Express 5
- MongoDB + Mongoose (thread & message persistence)
- OpenAI API (`gpt-4o-mini`)
- dotenv, cors, nodemon

---

## 📁 Project Structure

```
SigmaGPT/
├── Backend/
│   ├── models/
│   │   └── Thread.js         # Mongoose schema for chat threads
│   ├── routes/
│   │   └── chat.js           # API routes (chat, threads CRUD)
│   ├── utils/
│   │   └── openai.js         # OpenAI API call helper
│   └── server.js             # Express server entry point
│
└── Frontend/
    ├── src/
    │   ├── App.jsx            # Root component
    │   ├── Chat.jsx           # Chat input & logic
    │   ├── ChatWindow.jsx     # Message display window
    │   ├── Sidebar.jsx        # Thread list & navigation
    │   └── MyContext.jsx      # Global state context
    └── index.html
```

---

## 🚀 Getting Started

### Prerequisites

- Node.js (v18+)
- MongoDB (local or [MongoDB Atlas](https://www.mongodb.com/atlas))
- An [OpenAI API key](https://platform.openai.com/api-keys)

---

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/SigmaGPT.git
cd SigmaGPT
```

---

### 2. Backend Setup

```bash
cd Backend
npm install
```

Create a `.env` file in the `Backend/` directory:

```env
OPENAI_API_KEY=your_openai_api_key_here
MONGODB_URI=your_mongodb_connection_string_here
```

Start the backend server:

```bash
npm start
```

The server runs on **http://localhost:8080**

---

### 3. Frontend Setup

```bash
cd ../Frontend
npm install
npm run dev
```

The frontend runs on **http://localhost:5173**

---

## 🔌 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/thread` | Get all chat threads |
| `GET` | `/api/thread/:threadId` | Get messages for a specific thread |
| `POST` | `/api/chat` | Send a message and get AI reply |
| `DELETE` | `/api/thread/:threadId` | Delete a thread |

---

## ✨ Features

- 💬 Multi-turn conversations with OpenAI (`gpt-4o-mini`)
- 🧵 Persistent chat threads stored in MongoDB
- 📋 Sidebar with thread history, sorted by most recent
- 🗑️ Delete individual threads
- 📝 Markdown rendering with syntax-highlighted code blocks
- ⚡ Fast frontend with Vite + React

---

## 📸 Screenshots

> Add screenshots of your app here

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
