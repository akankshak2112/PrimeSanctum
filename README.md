# Prime Sanctum – Real Estate Platform

Prime Sanctum is a full-stack real estate web application that helps users explore property listings, filter properties based on their requirements, publish listings, save favourites, and communicate with other users.

The project was developed to gain practical experience in full-stack web development, REST API design, database management, authentication, and real-time communication.

## Features

- **User Authentication:** Registration and login using bcryptjs for password hashing and JWT for authentication.
- **Property Listings:** Browse available properties and view detailed property information.
- **Advanced Filtering:** Filter properties based on city, price range, number of bedrooms, and property type.
- **Create Listings:** Allow authenticated users to publish their own property listings.
- **User Profiles:** View and manage user profiles and property listings.
- **Saved Properties:** Save and remove favourite properties.
- **Real-Time Chat:** Communicate between buyers/renters and sellers using Socket.io.
- **Messaging System:** Create conversations and exchange messages.
- **Interactive Maps:** Display property locations using Leaflet and React Leaflet.

## Tech Stack

| Category | Technologies |
|---|---|
| Frontend | React.js, Vite, SCSS |
| Backend | Node.js, Express.js |
| Database | MongoDB |
| ORM | Prisma |
| Authentication | JWT, bcryptjs |
| Real-Time Communication | Socket.io |
| HTTP Requests | Axios |
| Maps | Leaflet, React Leaflet |
| State Management | Zustand |

## Project Structure

```text
Prime-Sanctum/
│
├── api/
│   ├── controllers/
│   ├── middleware/
│   ├── prisma/
│   ├── routes/
│   ├── lib/
│   └── app.js
│
├── client/
│   └── prime-sanctum/
│       └── src/
│           ├── components/
│           ├── context/
│           ├── lib/
│           ├── routes/
│           └── App.jsx
│
└── socket/
    └── app.js
```

## Installation and Setup

### Prerequisites

- Node.js
- npm
- MongoDB (local or MongoDB Atlas)
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/Prime-Sanctum.git
cd Prime-Sanctum
```

### 2. Backend Setup

Navigate to the API directory:

```bash
cd api
npm install
```

Create a `.env` file inside the `api` directory:

```env
DATABASE_URL="your_mongodb_connection_string"
JWT_SECRET_KEY="your_secret_key"
CLIENT_URL="http://localhost:5173"
```

Generate Prisma Client and synchronize the database:

```bash
npx prisma generate
npx prisma db push
```

Start the backend server:

```bash
node --watch app.js
```

Backend runs at:

```text
http://localhost:8800
```

### 3. Socket.io Setup

Open another terminal:

```bash
cd socket
npm install
node app.js
```

Socket.io server runs at:

```text
http://localhost:4000
```

### 4. Frontend Setup

Open another terminal:

```bash
cd client/prime-sanctum
npm install
npm run dev
```

Frontend runs at:

```text
http://localhost:5173
```

## API Routes

| Route | Description |
|---|---|
| `/api/auth` | User registration, login and logout |
| `/api/users` | User profiles and saved properties |
| `/api/posts` | Property listing operations |
| `/api/chats` | Conversation management |
| `/api/messages` | Messaging operations |
| `/api/test` | Testing endpoints |

## Future Improvements

- Complete property listing update functionality.
- Improve API validation and error handling.
- Enhance security and authorization.
- Add automated testing.
- Improve the user interface and responsiveness.
- Deploy the application for public access.

## Learning Outcomes

Through this project, I gained practical experience in:

- Developing full-stack web applications.
- Building RESTful APIs using Express.js.
- Managing MongoDB databases using Prisma ORM.
- Implementing authentication and authorization.
- Integrating real-time communication using Socket.io.
- Connecting frontend and backend services.

## License

See the LICENSE file for licensing information.
