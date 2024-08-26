# SecureAuthApp_with_session_cookies_and_env

This is a simple Express.js application that demonstrates user authentication using Passport.js with a PostgreSQL database. The application includes registration, login, and a protected secrets page.

## Features

- User registration with email and password
- User login and authentication
- Session management using `express-session`
- Password hashing with `bcrypt`
- Protected route that only authenticated users can access

## Setup

### 1. Clone the Repository

    ```bash
    git clone https://github.com/Manish312002/SecureAuthApp_with_session_cookies_and_env.git
    cd SecureAuthApp_with_session_cookies_and_env

### 2. Install Dependencies

     ```bash
     npm i express ejs pg body-parser bcrypt passport express-session passport-local dotenv

### 3. Configure Environment Variables

- Create a .env file in the root of your project with the following content:
    ```bash
    SESSION_SECRET=your_session_secret
    PG_USER=your_postgres_user
    PG_HOST=your_postgres_host
    PG_DATABASE=your_postgres_database
    PG_PASSWORD=your_postgres_password
    PG_PORT=your_postgres_port

### 4. Set Up the Database

- Ensure that your PostgreSQL database is running and create the necessary table for user authentication. You can use the following SQL command to create the table:
    ```bash
    CREATE TABLE userauth (
      id SERIAL PRIMARY KEY,
      email VARCHAR(255) UNIQUE,
      password varchar(255) NOT NULL
  );

### 5. Start the Application

     ```bash
    node index.js

## Usage

- Home Page: Access the home page at http://localhost:3000/.
- Register: Register a new user at http://localhost:3000/register.
- Login: Log in with an existing user at http://localhost:3000/login.
- Secrets: Access the secrets page (only available to authenticated users) at http://localhost:3000/secrets.
- Logout: Log out from the session at http://localhost:3000/logout.




