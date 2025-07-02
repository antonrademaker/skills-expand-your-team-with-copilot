# Mergington High School Activities

A comprehensive web application that allows teachers to manage and students to view and sign up for extracurricular activities at Mergington High School.

## Features

### Activity Management
- View all available extracurricular activities with detailed information
- Browse activities across multiple categories:
  - **Sports**: Soccer Team, Basketball Team, Morning Fitness
  - **Arts**: Art Club, Drama Club
  - **Academic**: Chess Club, Math Club, Debate Team, Science Olympiad
  - **Technology**: Programming Class, Weekend Robotics Workshop
  - **Community**: Manga Maniacs

### Search and Filtering
- **Text Search**: Search activities by name or description
- **Category Filtering**: Filter by activity type (Sports, Arts, Academic, Community, Technology)
- **Day Filtering**: Filter activities by specific days of the week (Monday-Sunday)
- **Time Filtering**: Filter by time slots:
  - Before School (6:00 AM - 8:00 AM)
  - After School (3:00 PM - 6:00 PM)
  - Weekend activities

### User Authentication
- Teacher login system with secure password hashing
- Session management and validation
- Role-based access control (Teacher/Admin roles)
- Persistent login sessions with browser storage

### Activity Registration
- Student signup for activities (requires teacher authentication)
- Student unregistration from activities
- Participant limit enforcement
- Real-time participant count display
- Duplicate registration prevention

### Technical Features
- Responsive web design
- Real-time activity loading
- Interactive modal dialogs for registration and login
- RESTful API backend
- MongoDB database integration

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/activities` | Get all activities with optional filtering by day and time |
| POST | `/activities/{activity_name}/signup` | Sign up a student for an activity (requires teacher auth) |
| POST | `/activities/{activity_name}/unregister` | Remove a student from an activity (requires teacher auth) |
| POST | `/auth/login` | Teacher authentication |
| GET | `/auth/check-session` | Validate teacher session |

## Sample Activities

The system comes pre-loaded with diverse activities including:
- **Chess Club** - Strategic thinking and tournaments (Mon/Fri 3:15-4:45 PM)
- **Programming Class** - Software development fundamentals (Tue/Thu 7:00-8:00 AM)
- **Soccer Team** - Competitive sports training (Tue/Thu 3:30-5:30 PM)
- **Art Club** - Creative arts and techniques (Thu 3:15-5:00 PM)
- **Weekend Robotics Workshop** - STEM learning (Sat 10:00 AM-2:00 PM)
- And many more across all time slots and categories

## Teacher Accounts

Default teacher accounts for testing:
- **Username**: `mrodriguez`, **Password**: `art123` (Ms. Rodriguez)
- **Username**: `mchen`, **Password**: `chess456` (Mr. Chen)  
- **Username**: `principal`, **Password**: `admin789` (Principal Martinez)

## Development Guide

For detailed setup and development instructions, please refer to our [Development Guide](../docs/how-to-develop.md).
