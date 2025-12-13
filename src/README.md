# Mergington High School Activities

A web application that allows students to view extracurricular activities and teachers to manage student registrations.

## Features

### For Students
- **View Activities**: Browse all available extracurricular activities with details including:
  - Activity description
  - Schedule (days and times)
  - Maximum participants
  - Current number of participants
- **Search & Filter**: Find activities using:
  - Text search by activity name
  - Category filters (Sports, Arts, Academic, Community, Technology)
  - Day filters (Monday through Sunday)
  - Time filters (Before School, After School, Weekend)

### For Teachers
- **Authentication**: Secure teacher login system
- **Student Registration**: Sign up students for activities
- **Student Unregistration**: Remove students from activities

## Architecture

### Frontend
- **HTML/CSS/JavaScript**: Simple, user-friendly interface
- **Features**:
  - Activity browsing with real-time filtering
  - Teacher authentication modal
  - Student registration modal
  - Responsive design

### Backend
- **FastAPI**: Modern Python web framework
- **MongoDB**: Database for storing activities and teacher accounts
- **API Endpoints**:
  - `GET /activities` - Retrieve all activities (with optional day/time filters)
  - `GET /activities/days` - Get list of available days
  - `POST /activities/{activity_name}/signup` - Register a student (requires teacher auth)
  - `POST /activities/{activity_name}/unregister` - Unregister a student (requires teacher auth)
  - `POST /auth/login` - Teacher login
  - `GET /auth/check-session` - Verify teacher session

### Technologies
- **Python** with FastAPI and Uvicorn
- **MongoDB** for data persistence
- **Argon2** for password hashing
- **HTML, CSS, JavaScript** for the frontend

## Development Guide

For detailed setup and development instructions, please refer to our [Development Guide](../docs/how-to-develop.md).
