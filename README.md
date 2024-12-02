# User Authentication with JWT and bcrypt.js

This project implements **User Authentication** using **Mongoose**, **bcrypt.js**, and **jsonwebtoken** for secure user management in a MongoDB database. It includes password hashing, token generation (access and refresh), and references for the user's watch history.

## Features

- **Password Hashing**:  
  - Uses `bcrypt.js` to securely hash user passwords before storing them in the database.

- **JWT Authentication**:  
  - Generates **Access Tokens** for user authentication with a short expiry time.
  - Generates **Refresh Tokens** for renewing access tokens without re-authentication.

- **User Data**:  
  - Stores user information such as `username`, `email`, `fullName`, and profile images.
  - Optionally stores watch history as references to videos.

- **Schema Validation**:  
  - Ensures required fields are present and provides indexing for fast queries (e.g., `username`, `email`).

- **Timestamps**:  
  - Automatically manages creation and update timestamps for each user document.

## Prerequisites

To use this project, ensure you have:

- **Node.js** installed on your machine.
- **MongoDB** instance running for storing user data.

### Required Environment Variables

Create a `.env` file in the root of your project and add the following:

```plaintext
ACCESS_TOKEN_SECRET=<your_access_token_secret>
ACCESS_TOKEN_EXPIRY=<access_token_expiry_time>
REFRESH_TOKEN_SECRET=<your_refresh_token_secret>
REFRESH_TOKEN_EXPIRY=<refresh_token_expiry_time>
