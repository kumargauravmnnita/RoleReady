# RoleReady

RoleReady is a production-ready full-stack AI-powered job preparation platform that enables users to upload resumes, analyze job descriptions, identify skill gaps, and generate personalized interview questions and ATS-optimized resumes.

This project simulates a real-world SaaS product with secure authentication, AI integration, and scalable architecture.

---

## Overview

RoleReady provides an end-to-end pipeline for job preparation:

1. User authentication and session management
2. Resume upload and parsing
3. Job description analysis
4. Skill extraction and gap detection
5. AI-generated interview questions and reports
6. ATS-optimized resume generation
7. Dynamic PDF creation

---

## Features

### Authentication & Security

- JWT-based authentication
- Secure cookie handling
- Token blacklisting for logout
- Protected routes with middleware

### Resume & AI Processing

- Resume upload using Multer
- Resume parsing and structured data extraction
- Skill extraction from resume and job description
- AI-powered skill gap detection
- Structured AI response validation using Zod

### Interview Preparation

- Generate personalized interview questions
- Store and retrieve interview reports
- View past reports (history system)
- Rehydration logic for state persistence

### Resume Generation

- ATS-optimized resume generation using AI
- Dynamic HTML-to-PDF conversion using Puppeteer
- Downloadable resume output

### Frontend Architecture

- Context API for global state management
- Custom hooks (useAuth, useInterview)
- Protected routing system
- Service layer abstraction using Axios

---

## Tech Stack

### Frontend

- React.js
- Vite
- React Router
- Context API
- Axios

### Backend

- Node.js
- Express.js

### Database

- MongoDB Atlas

### Authentication

- JWT (JSON Web Tokens)
- Token Blacklisting

### AI Integration

- Gemini API

### Other Tools

- Puppeteer (PDF generation)
- Multer (file upload handling)
- Zod (schema validation)

---

## Architecture

The application follows a layered architecture:

- Routes Layer (API endpoints)
- Controller Layer (request handling)
- Service Layer (business logic + AI integration)
- Model Layer (MongoDB schemas)

---

## Project Structure

RoleReady/
│
├── client/ # React frontend
│ ├── src/
│ │ ├── pages/
│ │ ├── components/
│ │ ├── hooks/
│ │ ├── context/
│ │ └── services/
│
├── server/ # Node.js backend
│ ├── controllers/
│ ├── routes/
│ ├── models/
│ ├── middleware/
│ ├── services/
│ └── utils/
│
└── README.md

---

## Installation

### Clone Repository

git clone https://github.com/your-username/roleready.git

cd roleready

### Backend Setup

cd server
npm install

Create `.env` file:

PORT=5000
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_secret
GEMINI_API_KEY=your_gemini_api_key

Run backend:

npm run dev

### Frontend Setup

cd ../client
npm install
npm run dev

---

## API Endpoints

### Auth

- POST `/api/auth/register`
- POST `/api/auth/login`
- POST `/api/auth/logout`
- GET `/api/auth/me`

### Interview

- POST `/api/interview/generate`
- GET `/api/interview`
- GET `/api/interview/:id`

### Resume

- POST `/api/resume/generate`

---

## Key Concepts Implemented

- Full-stack production architecture
- Secure authentication with token invalidation
- AI integration in real-world workflows
- Resume parsing and structured data handling
- State management using Context API
- Custom hooks for modular logic
- File uploads and processing
- Server-side PDF generation

---

## Future Improvements

- Real-time mock interview simulation
- Better resume parsing using NLP pipelines
- Job recommendation system
- Role-based dashboards
- Deployment with CI/CD
- Caching and performance optimization
