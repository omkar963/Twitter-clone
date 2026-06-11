# 🐦 Twiller - Twitter Clone (MERN Stack)

Twiller is a full-featured **Twitter Clone** built using the **MERN stack** — **MongoDB**, **Express**, **React**, and **Node.js** — with **Firebase Authentication** for secure login and Google sign-in support.  
It mimics core social media behavior such as posting tweets, editing profiles, and viewing timelines, all within a modern, responsive interface.

---

## 🚀 Features

- 🔐 **Authentication**
  - Firebase email/password login and Google Sign-In
  - Auth state persisted with React Context API

- 👥 **User Management**
  - Register, log in, and update user profiles
  - Logged-in user data fetched from backend MongoDB

- 🗨️ **Tweet / Post System**
  - Add, fetch, and display posts dynamically
  - User-specific and global feeds
  - Reverse chronological order (latest posts first)

- 🗄️ **Database**
  - MongoDB used for storing users and posts
  - Supports both local MongoDB and MongoDB Atlas (cloud)

- ⚙️ **Backend**
  - Node.js + Express REST API
  - CORS enabled for cross-origin access
  - Cleanly structured endpoints

- 💅 **Frontend**
  - React 18 + Material UI 5
  - Responsive Twitter-style layout
  - React Router v6 for navigation

---

## 🧩 Tech Stack

| Layer | Technology |
|--------|-------------|
| **Frontend** | React, React Router, Material UI |
| **Backend** | Node.js, Express |
| **Database** | MongoDB (Local or Atlas) |
| **Authentication** | Firebase (Email/Password & Google) |
| **State Management** | React Context API |

---


## ⚙️ Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/omkar963/Twitter-clone.git
cd Twitter-clone
2. Backend Setup (MongoDB + Express)
Navigate to your backend folder:

bash
Copy code
cd server
npm install
⚡ MongoDB Configuration
You have two options:

Option 1: Use MongoDB Atlas (Recommended)
Go to MongoDB Atlas.

Create a free cluster.

Create a database user and allow access from “Anywhere.”

Copy the connection string (it’ll look like this):

ruby
Copy code
mongodb+srv://<username>:<password>@cluster0.mongodb.net/?retryWrites=true&w=majority
Add it to your code or .env file as:

env
Copy code
MONGO_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/?retryWrites=true&w=majority
PORT=5000
Option 2: Use Local MongoDB
Install MongoDB Community Server.

During installation, choose “Run as Network Service user.”

Once installed, start MongoDB:

bash
Copy code
net start MongoDB
Use this URI in your code:

js
Copy code
const uri = "mongodb://127.0.0.1:27017";
3. Start the backend server
bash
Copy code
npm start
You should see:

vbnet
Copy code
Connected to MongoDB
Twiller clone backend running on port 5000
4. Frontend Setup (React)
In another terminal:

bash
Copy code
cd ../twiller
npm install
npm start
This launches the app on http://localhost:3000

📡 API Endpoints
Method	Endpoint	Description
POST	/register	Register a new user
GET	/loggedinuser?email=user@example.com	Fetch logged-in user data
POST	/post	Add a new tweet/post
GET	/post	Fetch all posts
GET	/userpost?email=user@example.com	Fetch posts by user
PATCH	/userupdate/:email	Update user profile

🔐 Firebase Setup
Go to Firebase Console

Create a new project.

Enable Email/Password and Google Authentication in the Authentication section.

Copy your Firebase config and paste it inside:

js
Copy code
// twiller/src/context/firebase.js
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID",
};
🧪 Running the App
Start backend: npm start inside /server

Start frontend: npm start inside /twiller

Open http://localhost:3000 to view the app.


🧑‍💻 Author
Omkar Mhamunkar
Full Stack Developer | MERN | Generative AI Enthusiast





