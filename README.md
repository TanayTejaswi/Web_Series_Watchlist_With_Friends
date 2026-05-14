# 🎬 Web Series Watchlist

A full-stack web application built with **Node.js, Express.js, EJS, and MySQL** that allows users to discover web series, manage personalized watchlists, connect with friends, and explore content by genre.

The platform includes secure authentication with OTP verification, a friendship system, live search, genre-based browsing, and detailed series pages with seasons and episodes.


# Features

# Authentication System
- User Registration & Login
- Secure password hashing using **bcrypt**
- OTP-based email verification
- Session-based authentication

---

## Series Discovery
- Browse trending web series
- Explore series by genre
- Detailed series information pages
- Seasons & episodes support
- Recommended series section

---

##  Watchlist Management
- Add series to watchlist
- Remove series from watchlist
- Personalized watchlist dashboard

---

##  Friendship System
- Send friend requests
- Accept friend requests
- Remove friends
- View friends list
- Explore friends’ watchlists

---

## 🔍 Search Functionality
- Live search suggestions
- Full search results page
- Genre-aware filtering

---

##  User Profile
- Profile dashboard
- Friends overview
- Watchlist statistics

---

# Tech Stack

## Backend
- Node.js
- Express.js

## Frontend
- EJS
- HTML5
- CSS3
- JavaScript

## Database
- MySQL

## Authentication & Utilities
- bcrypt
- express-session
- dotenv
- nodemailer

---

#  Project Structure

```text
project/
│
├── public/                  # Static assets (CSS, JS, images)
├── utils/                   # Utility functions & custom error handlers
├── views/
│   ├── pages/               # Main EJS pages
│   └── partials/            # Reusable EJS components
│
├── database/
│   └── schema.sql           # Database schema
│
├── .env.example             # Example environment variables
├── .gitignore
├── app.js                   # Main server file
├── package.json
├── package-lock.json
└── README.md
```

---

#  Installation & Setup

1. Clone the Repository

```bash
git clone https://github.com/your-username/your-repository-name.git
```

---

2. Navigate to the Project Directory

```bash
cd your-repository-name
```

---

3. Install Dependencies

```bash
npm install
```

---

4. Setup MySQL Database

Create a MySQL database:

```sql
CREATE DATABASE watchlist;
```

Import the SQL schema:

### Using MySQL Workbench
- Open `database/schema.sql`
- Execute the script

### OR Using Terminal

```bash
mysql -u root -p watchlist < database/schema.sql
```

---

5. Configure Environment Variables

Create a `.env` file in the root directory.

Example:

```env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=watchlist

EMAIL=your_email@gmail.com
EMAIL_PASS=your_email_app_password
```

---

6. Start the Server

```bash
node app.js
```

Server will run at:

```text
http://localhost:3000
```

---

# Main Routes

| Route | Description |
| `/watchlist/login` | User login |
| `/watchlist/register` | User registration |
| `/watchlist/home` | Homepage |
| `/watchlist/genre/:id` | Browse by genre |
| `/watchlist/series/:id` | Series details page |
| `/watchlist/profile` | User profile |
| `/watchlist/search` | Search page |
| `/watchlist/friends` | Friendship system |
| `/watchlist` | User watchlist |

---

Recommended MySQL connection setup:

const connection = mysql.createConnection({
  host: process.env.DB_HOST,
  user: process.env.DB_USER,
  database: process.env.DB_NAME,
  password: process.env.DB_PASSWORD,
});


Developed by **Tanay**
