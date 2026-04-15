# 🟢 Basic Node.js HTTP Server

A minimal HTTP server built with Node.js's built-in `node:http` module — no frameworks, no external dependencies, just pure Node.js.

---

## 📖 About

This project demonstrates how to create a basic HTTP server using only Node.js core modules. It's the perfect starting point for understanding how web servers work under the hood before moving on to frameworks like Express.js.

---

## 🛠 Tech Stack

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)

- **Runtime:** Node.js
- **Module:** `node:http` *(built-in — zero dependencies)*

---

## 📁 Project Structure

```
my-node-server/
│
├── server.js       ← HTTP server entry point
├── package.json    ← Project metadata
├── .gitignore      ← Git ignore rules
└── README.md       ← You are here
```

---

## ⚙️ Prerequisites

Ensure Node.js is installed on your machine:

```bash
node --version    # v14.0.0 or higher recommended
```

> Don't have Node.js? Download it at [nodejs.org](https://nodejs.org)

---

## 🚀 Getting Started

**1. Clone the repository**

```bash
git clone https://github.com/yourusername/my-node-server.git
cd my-node-server
```

**2. Start the server**

```bash
node server.js
```

**3. Open your browser and visit**

```
http://localhost:3000
```

You should see → **Hello World**

---

## 💻 Source Code

```javascript
const { createServer } = require("node:http");

const server = createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader("Content-Type", "text/plain");
  res.end("Hello World");
});

server.listen(3000, () => {
  console.log(`Server running at http://localhost:3000/`);
});
```

---

## 🔍 Code Breakdown

| Code | What It Does |
|------|-------------|
| `require("node:http")` | Imports Node's built-in HTTP module |
| `createServer()` | Creates the server instance |
| `req` | Incoming request — contains URL, method, headers |
| `res` | Outgoing response — sent back to the client |
| `res.statusCode = 200` | HTTP status OK |
| `res.setHeader()` | Sets the response content type |
| `res.end("Hello World")` | Sends response and closes the connection |
| `server.listen(3000)` | Boots the server on port 3000 |

---

## 📌 Concepts Covered

- ✅ HTTP server creation with zero dependencies
- ✅ Understanding `req` (request) and `res` (response)
- ✅ Setting HTTP status codes
- ✅ Writing response headers
- ✅ Listening on a network port

---

## 🗺️ Roadmap

```
✅ Basic HTTP Server        ← You are here
      ↓
   Multiple Routes
      ↓
   Express.js
      ↓
   REST API
      ↓
   Database Integration
      ↓
   Deploy 🚀
```

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 👨‍💻 Author

**Your Name**  
GitHub: [@KunalGuhagarkar](https://github.com/KunalGuhagarkar)

---

> 💡 *Built while learning Node.js — one server at a time.*
