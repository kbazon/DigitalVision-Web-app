# DigitalVision Web App

DigitalVision is a full-stack web application for exploring, publishing, and saving digital artwork. The application allows users to register, log in, browse artwork, search through available art, add favorites, manage their profile, and send contact messages through the contact form.

## Features

* User registration and login
* Digital artwork search and exploration
* User profile page
* Add and remove favorite artwork
* Add user artwork
* Contact form with email sending
* Responsive frontend built with Quasar and Vue
* REST API built with Express.js
* MySQL database integration

## Tech Stack

### Frontend

* Vue 3
* Quasar Framework
* Vue Router
* Axios
* SCSS

### Backend

* Node.js
* Express.js
* MySQL
* Nodemailer
* Jest
* Supertest

## Project Structure

```text
DigitalVision-Web-app/
├── backend/
│   ├── indeks.js
│   ├── init.sql
│   ├── package.json
│   └── favoriti.test.js
│
├── frontend/
│   └── digital-vision-projekt/
│       ├── src/
│       │   ├── pages/
│       │   ├── layouts/
│       │   ├── router/
│       │   └── css/
│       ├── public/
│       ├── package.json
│       └── quasar.config.js
│
├── install.bat
└── README.md
```

## Main Pages

```text
/               Home page
/pretrazivanje  Explore and search artwork
/onama          About us page
/kontakt        Contact page
/prijava        Login page
/reg            Registration page
/profil         User profile page
```

## Backend API Endpoints

```text
POST /api/login
POST /api/reg
GET  /api/search
POST /api/add-to-favorites
GET  /api/user-favorites
POST /api/remove-from-favorites
GET  /api/slike-umj
POST /api/add-art
POST /send-email
```

## Requirements

Before running the project, install:

* Node.js 18 or 20
* npm
* MySQL

## Environment Variables

Create a `.env` file inside the `backend` folder.

```env
DB_HOST=localhost
DB_USER=your_mysql_user
DB_PASSWORD=your_mysql_password
DB_NAME=kbazon

SMTP_USER=your_email@gmail.com
SMTP_PASS=your_app_password
```

Do not commit the `.env` file to GitHub.

A safe example file can be committed as `.env.example`:

```env
DB_HOST=
DB_USER=
DB_PASSWORD=
DB_NAME=

SMTP_USER=
SMTP_PASS=
```

## Database Setup

Create the database and tables using the SQL script:

```bash
cd backend
mysql -u root -p < init.sql
```

The script creates the required tables:

* `Artist`
* `Art`
* `Favorites`

## Installation and Running

### 1. Run the backend

```bash
cd backend
npm install
npm install dotenv
node indeks.js
```

Backend runs on:

```text
http://localhost:3000
```

### 2. Run the frontend

Open a new terminal:

```bash
cd frontend/digital-vision-projekt
npm install
npm run dev
```

Frontend runs on:

```text
http://localhost:9000
```

## Running Tests

Backend tests:

```bash
cd backend
npm test
```

Frontend linting:

```bash
cd frontend/digital-vision-projekt
npm run lint
```

## Author

Created by kbazon.
