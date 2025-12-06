## Real Talk

Real Talk is a real-time chat application built using the MERN stack (MongoDB, Express.js, React, and Node.js). It allows users to sign up, sign in, and chat with other users in real time. The app utilizes Vite as a build tool, Socket.IO for real-time communication, Daisy UI for styling, JWT for authentication, and Tailwind CSS for UI components. The app is deployed on Render.




## Features

- User sign up: New users can create an account by signing up with a unique username and password.
- User sign in: Registered users can sign in using their credentials to access the chat functionality.
- Real-time chat: Users can engage in real-time conversations with other users, allowing for instant messaging.
- Secure authentication: JWT is used for secure authentication and authorization of users.
- Responsive UI: The app is designed to provide a seamless experience across different devices and screen sizes.



## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/mhatreojas/Whispr
   cd Whispr
   ```

2. Set up environment variables:

   **Backend (.env in root directory):**
   ```bash
   cp .env.example .env
   ```
   Edit `.env` and add your MongoDB URI, JWT secret, and other configuration.

   **Frontend (client/.env):**
   ```bash
   cd client
   cp .env.example .env
   ```
   For development, the default `VITE_API_BASE_URL=http://localhost:5000` works.
   For production, set it to your backend URL or leave empty if deployed together.

3. Install dependencies:

   ```bash
   # Install backend dependencies (from root)
   npm install
   
   # Install frontend dependencies
   cd client
   npm install
   cd ..
   ```

## Usage

### Development

1. Start the backend server (from root directory):

   ```bash
   npm run dev
   ```

2. In a new terminal, start the frontend (from root directory):

   ```bash
   cd client
   npm run dev
   ```

3. Open your browser and navigate to `http://localhost:3000`

### Production

1. Build the application:

   ```bash
   npm run build
   ```

2. Start the production server:

   ```bash
   npm start
   ```

   The application will serve both frontend and backend on the configured PORT (default: 5000).

## Environment Variables

### Backend (.env)
- `PORT` - Server port (default: 5000)
- `MONGO_DB_URI` - MongoDB connection string
- `JWT_SECRET` - Secret key for JWT tokens
- `NODE_ENV` - Environment mode (development/production)

### Frontend (client/.env)
- `VITE_API_BASE_URL` - Backend API URL
  - Development: `http://localhost:5000`
  - Production: Leave empty to use same domain, or set to your backend URL

# Future Enhancements

- User profiles: Allow users to customize their profiles with avatars, status messages, etc.
- Group chats: Implement the ability for users to create and participate in group chats.
- File sharing: Enable users to share files with each other during chat sessions.
- Notifications: Implement real-time notifications for new messages and other events.
- Emojis and reactions: Add support for emojis and message reactions.

