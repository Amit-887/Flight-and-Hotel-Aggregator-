# TravelEase - MERN Stack Flight & Hotel Booking Application

A full-stack web application for booking flights and hotels built with the MERN stack (MongoDB, Express.js, React.js, Node.js).

## Features

### Backend Features
- **User Authentication**: JWT-based authentication system
- **Flight Search**: Integration with Amadeus API for real-time flight data
- **Hotel Management**: CRUD operations for hotel listings
- **Booking System**: Complete booking management with status tracking
- **RESTful API**: Well-structured API endpoints
- **Database**: MongoDB with Mongoose ODM

### Frontend Features
- **Modern React UI**: Built with React 18 and modern hooks
- **Responsive Design**: Mobile-first responsive design
- **Flight Search**: Real-time flight search with autocomplete
- **Hotel Filtering**: Advanced filtering by location, price, and rating
- **User Dashboard**: Booking history and profile management
- **Authentication**: Login/Register functionality

## Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM for MongoDB
- **JWT** - Authentication
- **Bcrypt** - Password hashing
- **Axios** - HTTP client for API calls
- **Helmet** - Security middleware
- **CORS** - Cross-origin resource sharing

### Frontend
- **React.js** - Frontend framework
- **React Router** - Client-side routing
- **Axios** - HTTP client
- **Tailwind CSS** - Utility-first CSS framework
- **Lucide React** - Icon library

## Installation & Setup

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or cloud)
- Amadeus API credentials

### Backend Setup

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd travelease-mern
   ```

2. **Install backend dependencies**
   ```bash
   npm install
   ```

3. **Environment Configuration**
   Create a `.env` file in the root directory:
   ```env
   NODE_ENV=development
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/travelease
   JWT_SECRET=your_jwt_secret_key_here
   AMADEUS_API_KEY=your_amadeus_api_key
   AMADEUS_API_SECRET=your_amadeus_api_secret
   ```

4. **Seed the database**
   ```bash
   node utils/seedData.js
   ```

5. **Start the backend server**
   ```bash
   npm run dev
   ```

### Frontend Setup

1. **Navigate to client directory**
   ```bash
   cd client
   ```

2. **Install frontend dependencies**
   ```bash
   npm install
   ```

3. **Start the React development server**
   ```bash
   npm start
   ```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get current user

### Flights
- `GET /api/flights/locations?keyword=` - Search locations
- `GET /api/flights/search` - Search flights
- `POST /api/flights/price` - Get flight pricing

### Hotels
- `GET /api/hotels` - Get all hotels (with filtering)
- `GET /api/hotels/:id` - Get single hotel
- `POST /api/hotels` - Create hotel
- `PUT /api/hotels/:id` - Update hotel
- `DELETE /api/hotels/:id` - Delete hotel

### Bookings
- `POST /api/bookings` - Create booking
- `GET /api/bookings` - Get user bookings
- `GET /api/bookings/:id` - Get single booking
- `PUT /api/bookings/:id` - Update booking
- `DELETE /api/bookings/:id` - Cancel booking

## Project Structure

```
travelease-mern/
├── client/                 # React frontend
│   ├── public/
│   ├── src/
│   │   ├── components/     # React components
│   │   ├── pages/         # Page components
│   │   ├── context/       # React context
│   │   ├── utils/         # Utility functions
│   │   └── App.js
│   └── package.json
├── models/                # MongoDB models
│   ├── User.js
│   ├── Hotel.js
│   └── Booking.js
├── routes/                # Express routes
│   ├── auth.js
│   ├── flights.js
│   ├── hotels.js
│   └── bookings.js
├── middleware/            # Custom middleware
│   └── auth.js
├── utils/                 # Utility functions
│   └── seedData.js
├── server.js             # Express server
├── package.json
└── .env
```

## Usage

1. **Register/Login**: Create an account or login with existing credentials
2. **Search Flights**: Use the flight search with origin, destination, and dates
3. **Browse Hotels**: Filter hotels by location, price range, and rating
4. **Make Bookings**: Book flights or hotels and track them in your dashboard
5. **Manage Profile**: View booking history and update profile information

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

Your Name - your.email@example.com
Project Link: [https://github.com/yourusername/travelease-mern](https://github.com/yourusername/travelease-mern)
