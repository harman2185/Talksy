# Talksy - Real-Time Chat Application

A modern, full-stack real-time chat application built with **React**, **Express.js**, **Socket.io**, and **MongoDB**.

## Features

- 🔐 **User Authentication** - Secure signup and login with JWT and OTP verification
- 💬 **Real-Time Messaging** - Instant message delivery using Socket.io
- 👥 **User Profiles** - Manage user profiles with avatar uploads via Cloudinary
- 🎨 **Theme Support** - Dark/Light mode toggle for personalized experience
- 📱 **Responsive Design** - Works seamlessly on desktop and mobile devices
- 🖼️ **Image Support** - Share images and media in conversations
- ⚡ **Fast & Performant** - Built with modern technologies for optimal performance

## Tech Stack

### Frontend
- **React 19** - UI library
- **Vite** - Fast build tool
- **TailwindCSS** - Utility-first CSS framework
- **Zustand** - State management
- **Socket.io-client** - Real-time communication
- **React Router** - Client-side routing
- **Axios** - HTTP client
- **React Hot Toast** - Notifications

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Socket.io** - Real-time bidirectional communication
- **JWT** - Authentication
- **Cloudinary** - Image storage and management
- **Nodemailer** - Email notifications
- **Mongoose** - MongoDB ODM
- **Bcrypt** - Password hashing

## Installation

### Prerequisites
- Node.js (v16 or higher)
- MongoDB
- npm or yarn

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/harman2185/Talksy.git
   cd Talksy
   ```

2. **Backend Setup**
   ```bash
   cd backend
   npm install
   
   # Create .env file with the required variables
   cp .env.example .env
   # Edit .env and fill in your configuration
   
   cd ..
   ```

3. **Frontend Setup**
   ```bash
   cd frontend
   npm install
   cd ..
   ```

## Configuration

### Backend Environment Variables (.env)
```
PORT=8080
NODE_ENV=development
MONGO_URL=mongodb://localhost:27017/talksy
JWT_SECRET=your_jwt_secret_key_here
OTP_SECRET=your_otp_secret_key_here
EMAIL=your_email@gmail.com
PASSWORD=your_app_password
CLOUDINARY_CLOUD_NAME=your_cloudinary_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
```

## Running the Project

### Development Mode

1. **Start Backend Server** (from root directory)
   ```bash
   npm run start --prefix backend
   ```
   Or with hot reload:
   ```bash
   npm run dev --prefix backend
   ```

2. **Start Frontend Server** (in a new terminal)
   ```bash
   npm run dev --prefix frontend
   ```

The frontend will be available at `http://localhost:5173` and the backend API at `http://localhost:8080`

### Build for Production

```bash
npm run build
```

This will:
- Install all dependencies for both frontend and backend
- Build the frontend for production

## Project Structure

```
Talksy/
├── backend/
│   ├── src/
│   │   ├── controllers/      # Route controllers
│   │   ├── models/          # MongoDB schemas
│   │   ├── routes/          # API endpoints
│   │   ├── middleware/      # Express middleware
│   │   ├── lib/             # Utilities (db, socket, cloudinary)
│   │   └── index.js         # Entry point
│   └── package.json
├── frontend/
│   ├── src/
│   │   ├── components/      # React components
│   │   ├── pages/          # Page components
│   │   ├── store/          # Zustand stores
│   │   ├── lib/            # Utilities
│   │   ├── constants/      # App constants
│   │   └── main.jsx        # Entry point
│   └── package.json
└── package.json
```

## API Endpoints

### Authentication
- `POST /api/auth/signup` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `GET /api/auth/profile` - Get user profile
- `PUT /api/auth/profile` - Update user profile

### Messages
- `GET /api/messages/:userId` - Get conversation with user
- `POST /api/messages/send/:id` - Send message to user
- `GET /api/messages/users` - Get list of conversations

## Features in Detail

### Authentication
- Email/Password signup and login
- JWT token-based authentication
- Optional OTP verification
- Secure password hashing with bcrypt

### Real-Time Chat
- Socket.io for instant message delivery
- Online/offline status
- Typing indicators
- Read receipts

### User Management
- Profile customization
- Avatar upload to Cloudinary
- User search and discovery
- Conversation history

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the ISC License.

## Support

For support, please open an issue on the GitHub repository.

---

**Built with ❤️ by Harman**
