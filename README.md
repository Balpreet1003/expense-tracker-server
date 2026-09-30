# AI-Powered Expense Tracker – Backend

A secure and scalable backend for the **AI-Powered Expense Tracker**, built with Node.js and Express.js. It provides RESTful APIs for authentication, financial data management, dashboard analytics, profile management, data export, and AI-powered financial insights.

<p align="center">

<img src="https://img.shields.io/badge/Node.js-Express-green?logo=node.js">

<img src="https://img.shields.io/badge/PostgreSQL-Database-blue?logo=postgresql">

<img src="https://img.shields.io/badge/Redis-Cache-red?logo=redis">

<img src="https://img.shields.io/badge/Gemini-AI-orange">

<img src="https://img.shields.io/badge/Cloudinary-Cloud%20Storage-blue?logo=cloudinary">

</p>

---

## Table of Contents

- [Live Demo](#live-demo)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [System Architecture](#system-architecture)
- [Installation](#installation)
- [API Endpoints](#api-endpoints)
- [Security Features](#security-features)
- [Performance Optimizations](#performance-optimizations)

---

## Live Demo

⚙️ **Backend API:**  
https://expense-tracker-wjx8.vercel.app

---

## Features

- RESTful APIs for authentication, financial data, transactions, and dashboard management
- PostgreSQL integration for securely storing and managing user financial data
- JWT-based authentication and authorization with bcrypt password hashing
- AI-powered financial analysis using Gemini with personalized user data context
- Cloudinary image storage and Excel export for profile and financial data management

---

## Tech Stack

### Runtime

- Node.js

### Backend Framework

- Express.js

### Database

- PostgreSQL

### Authentication

- JSON Web Token (JWT)
- bcrypt

### AI

- Google Gemini API
- Tool-Augmented RAG
- pgvector
- Prompt Engineering

### Caching

- Redis

### Cloud Storage

- Cloudinary

### File Handling

- Multer

### Data Export

- XLSX

### API Development

- REST APIs
- Axios
- CORS

### Environment Management

- dotenv

### Development

- Nodemon

### Deployment

- Vercel

---

## System Architecture

```text
                           Client Application
                                   │
                                   ▼
                              Express Server
                                   │
             ┌─────────────────────┼─────────────────────┐
             │                     │                     │
             ▼                     ▼                     ▼
      Authentication         Finance APIs            AI Agent
             │                     │                     │
             ▼                     ▼                     ▼
        JWT + bcrypt       PostgreSQL          Tool Planner
                                                        │
                               ┌────────────────────────┴────────────────────────┐
                               │                                                 │
                               ▼                                                 ▼
                        SQL Analytics                                      Vector Search
                                                                         PostgreSQL + pgvector
                               │                                                 │
                               └────────────────────────┬────────────────────────┘
                                                        │
                                                        ▼
                                                   Gemini API
                                                        │
                                                        ▼
                                             Personalized Response
```

---

## Installation

### Clone the Repository

```bash
https://github.com/Balpreet1003/expense-tracker-server.git
```

---

### Install Dependencies

```bash
npm install
```

---

### Environment Variables

Create a `.env` file in the backend directory:

```env
PORT=5000

DATABASE_URL=your_postgresql_connection_string

JWT_SECRET=your_jwt_secret

GEMINI_API_KEY=your_gemini_api_key

REDIS_URL=your_redis_connection_string

CLOUDINARY_CLOUD_NAME=your_cloud_name

CLOUDINARY_API_KEY=your_cloudinary_api_key

CLOUDINARY_API_SECRET=your_cloudinary_api_secret

FRONTEND_URL=http://localhost:5173
```

---

### Start Development Server

```bash
npm run dev
```

The backend will typically run at:

```text
http://localhost:5000
```

---

### Start Production Server

```bash
npm start
```

---

## API Endpoints

### Authentication

```text
/api/v1/auth/*
```

Handles:

- User registration
- User login
- User authentication
- Profile management

---

### Dashboard

```text
/api/v1/dashboard/*
```

Provides:

- Financial overview
- Income summaries
- Expense summaries
- Recent financial activity
- Dashboard analytics

---

### Income

```text
/api/v1/income/*
```

Handles:

- Income records
- Income history
- Income analytics
- Excel export

---

### Expense

```text
/api/v1/expense/*
```

Handles:

- Expense records
- Expense history
- Expense analytics
- Excel export

---

### Transactions

```text
/api/v1/transaction/*
```

Handles:

- Add transactions
- Retrieve transaction history
- Delete transactions
- Transaction export

---

### Cards

```text
/api/v1/cards/*
```

Handles:

- Add financial cards
- Retrieve cards
- Update card information
- Delete cards

---

### AI Agent

```text
/api/v1/ai/*
```

Handles:

- Financial questions
- Transaction analysis
- Personalized financial insights
- AI-powered responses

---

## Security Features

- JWT-based authentication and authorization for protected API access
- Password hashing using bcrypt before storing user credentials
- User-specific authorization to prevent unauthorized access to financial data
- Environment variables for protecting API keys and sensitive configuration
- Input validation, error handling, CORS configuration, and secure file uploads

---

## Performance Optimizations

- Redis caching for frequently accessed and AI-generated responses
- Optimized SQL queries and PostgreSQL materialized views for financial analytics
- Vector similarity search using pgvector for efficient knowledge retrieval
- Modular backend architecture for maintainability and efficient request handling
- Efficient REST API design with structured database queries and response handling
