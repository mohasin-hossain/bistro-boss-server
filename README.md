# Bistro Boss Restaurant - Backend

Welcome to the backend of the **Bistro Boss Restaurant** web application. This server handles all the logic and data management for the restaurant, including user authentication, order management, reservations, and more.

## Features

### User Features:
- **Authentication**
  - Email/password registration
  - Google sign-in for easier user authentication
  - CAPTCHA for enhanced login security
  - Firebase Authentication for secure sign-ups and sign-ins

- **Order Management**: Handle and manage user orders, including order statuses.
  
- **Reservation System**: Handle table reservations and bookings.
  
- **Payment Integration**: Integration with Stripe for processing payments securely.

- **User Messaging**: Users can send messages to admins for feedback or queries.
  
- **Order History**: Retrieve past orders and booking information.

### Admin Features:
- **Admin Dashboard**:  
  - View and manage total revenue
  - Manage user roles and permissions
  - Control menu items (add, update, or delete items)
  - Manage orders with status updates (Accepted, Cooking, Packaging, etc.)
  - Manage table reservations (Confirm, Cancel, or Delete)
  
- **Messaging System**: Handle messages sent by users.

## Tech Stack
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: Firebase Authentication, JWT (JSON Web Tokens)
- **Payment**: Stripe API
- **Security**: CAPTCHA Integration
- **Deployment**: Railway

## Installation

### Prerequisites:
1. **Node.js**: Ensure that you have Node.js installed on your machine. You can download it from [here](https://nodejs.org/).
2. **MongoDB**: Set up a MongoDB database, either locally or using a service like [MongoDB Atlas](https://www.mongodb.com/cloud/atlas).

### Setup:
1. Clone the repository:
    ```bash
    git clone https://github.com/mohasin-hossain/bistro-boss-server.git
    cd bistro-boss-server
    ```
2. Install dependencies:
    ```bash
    npm install
    ```

3. Create a `.env` file in the root directory and add the following environment variables:

    ```env
    MONGO_URI=your_mongodb_connection_string
    STRIPE_SECRET_KEY=your_stripe_secret_key
    FIREBASE_API_KEY=your_firebase_api_key
    JWT_SECRET=your_jwt_secret_key
    ```

4. Run the server:
    ```bash
    npm start
    ```

5. The server should now be running at `http://localhost:5000`.

## API Documentation

Here is an overview of the available API endpoints:

- **POST /api/auth/register**: Register a new user
- **POST /api/auth/login**: User login (supports email/password and Google sign-in)
- **POST /api/orders**: Place a new order
- **GET /api/orders**: Get all orders (Admin)
- **POST /api/payments**: Make a payment using Stripe
- **GET /api/reservations**: Get table reservations (Admin)
- **POST /api/reservations**: Create a table reservation

For detailed API documentation, refer to the Postman collection or API documentation within the project.

## Deployment

- The backend is deployed on **Railway** and can be accessed at:  
  [https://bistro-boss-server-production-5043.up.railway.app/](https://bistro-boss-server-production-5043.up.railway.app/)

## Contributing

If you want to contribute to this project, follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to your branch (`git push origin feature-branch`).
5. Create a new pull request.

## Acknowledgements
- Firebase for user authentication
- Stripe for payment processing
- MongoDB for data storage
- Express.js for server-side logic
- React.js for frontend (integrated with this backend)
