# Chess Master Backend

The backend server for Chess Master, handling game logic, user authentication, and real-time gameplay.

## 🌐 Live Demo

[Chess Master Backend API](https://chess-backend-mo0t.onrender.com)

## 🛠️ Tech Stack

- Node.js
- Express.js
- Socket.IO (Real-time Communication)
- MongoDB (Database)
- JWT Authentication
- Bcrypt (Password Hashing)

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- MongoDB

### Installation

1. Clone the repository
```bash
git clone https://github.com/Lokesh-reddy18/chess-backend.git
cd backend
```

2. Install Dependencies
```bash
npm install
```

3. Set up environment variables
Create a `.env` file in the root directory:
```env
PORT=10000
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
FRONTEND_URL=https://chess-frontend-lokesh-reddy18s-projects.vercel.app
```

4. Start Development Server
```bash
npm start
```

## 📦 Project Structure

```
backend/
├── config/         # Configuration files
├── controllers/    # Route controllers
├── middlewares/    # Custom middlewares
├── models/         # Database models
├── routes/         # API routes
├── services/       # Business logic
├── server.js       # Entry point
└── package.json
```

## 🔒 Security Features

- JWT-based authentication
- Secure password hashing with bcrypt
- CORS protection
- Rate limiting
- Input validation
- Secure session management

## 📡 API Endpoints

### Authentication
- POST `/user/register` - Register new user
- POST `/user/login` - User login
- POST `/user/logout` - User logout
- GET `/profile` - Get user profile

### Game Management
- GET `/game/status` - Get game status
- POST `/game/move` - Make a move
- GET `/game/history` - Get game history

### User Management
- GET `/user/stats` - Get user statistics
- PUT `/user/profile` - Update user profile
- GET `/user/match-history` - Get match history

## 🔄 WebSocket Events

- `connection` - New client connection
- `disconnect` - Client disconnection
- `joinGame` - Join a game
- `makeMove` - Make a chess move
- `gameOver` - Game completion
- `opponentDisconnected` - Opponent left the game

## 📊 Database Schema

### User
```javascript
{
  username: String,
  email: String,
  password: String (hashed),
  rating: Number,
  matchHistory: Array
}
```

### Game
```javascript
{
  players: Array,
  moves: Array,
  status: String,
  result: String,
  startTime: Date,
  endTime: Date
}
```

## 👥 Author

Kolli Lokesh Reddy

## 📝 License

This project is licensed under the MIT License. 
