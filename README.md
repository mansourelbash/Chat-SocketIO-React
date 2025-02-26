# Build Chat App with React, Socket.io, Node.js, Redux-Toolkit, MongoDB (2025)

## Introduction
This project is a real-time chat application built using modern web technologies, including:

- **React.js** (Frontend UI)
- **Socket.io** (Real-time communication)
- **Node.js** with **Express.js** (Backend API)
- **Redux Toolkit** (State Management)
- **MongoDB** (Database)
- **Cloudinary** (Image Uploads)

This guide will walk you through setting up and running the application step-by-step.

## Features
- Real-time messaging
- User authentication (JWT-based)
- Online/offline status updates
- Group chat functionality
- Image upload support (via Cloudinary)
- Optimized state management with Redux Toolkit
- Secure database handling with MongoDB

---

## Project Setup

### Prerequisites
Ensure you have the following installed:
- **Node.js** (v16+ recommended)
- **MongoDB** (local or cloud-based like MongoDB Atlas)
- **NPM or Yarn**
- **Cloudinary Account** (for storing images)

### Installation
#### Clone the repository
```sh
git clone https://github.com/your-username/chat-app.git
cd chat-app
```
#### Install dependencies
##### Backend Setup
```sh
cd server
npm install
```
##### Frontend Setup
```sh
cd client
npm install
```

---

## Environment Variables
### Server (`server/.env`)
Create a `.env` file in the `server` directory and add the following:
```sh
FRONTEND_URL=<Frontend URL>
MONGODB_URI=<Your MongoDB URI>
JWT_SECRET_KEY=<Your JWT Secret Key>
```

### Client (`client/.env`)
Create a `.env` file in the `client` directory and add the following:
```sh
REACT_APP_CLOUDINARY_CLOUD_NAME=<Your Cloudinary Cloud Name>
REACT_APP_BACKEND_URL=<Your Backend API URL>
```

---

## Running the Application
### Start the Backend Server
```sh
cd server
npm run dev
```
By default, the backend runs on **http://localhost:5000**

### Start the Frontend
```sh
cd client
npm start
```
By default, the frontend runs on **http://localhost:3000**

---

## API Endpoints
### Authentication
- **POST** `/api/auth/register` - Register a new user
- **POST** `/api/auth/login` - Authenticate user
- **GET** `/api/auth/user` - Get logged-in user info

### Chat & Messages
- **GET** `/api/chat` - Fetch all chats
- **POST** `/api/chat` - Create a new chat
- **POST** `/api/message` - Send a new message
- **GET** `/api/message/:chatId` - Get messages for a chat

### User Management
- **GET** `/api/users` - Fetch all users
- **GET** `/api/users/:id` - Get a specific user

---

## Technologies Used
- **Frontend**: React.js, Redux Toolkit, Tailwind CSS, Socket.io-client
- **Backend**: Node.js, Express.js, Socket.io, MongoDB, Mongoose, JWT Authentication
- **Database**: MongoDB (Atlas or Local)
- **Storage**: Cloudinary (for image uploads)

---

## Deployment
### Deploying Backend (Node.js)
You can deploy the backend using **Heroku**, **Vercel**, or **Render**.
```sh
git push heroku main
```

### Deploying Frontend (React)
You can deploy the frontend using **Vercel**, **Netlify**, or **Firebase Hosting**.
```sh
npm run build
```
Upload the `build` folder to your preferred hosting service.

---

## Contributing
Feel free to contribute to the project by creating a pull request.
1. Fork the repository.
2. Create a new branch (`new-branch`).
3. Commit your changes.
4. Push your branch and create a Pull Request.
