
# Online Examination System - React.js Web Application

## Project Overview

A comprehensive offline-capable online examination system built with React.js for deployment on local networks (LAN/Wi-Fi hotspot). Supports multiple user roles with robust exam features and anti-cheating measures.

## Features

### Core Functionality
- **Multi-role authentication**: Admin, Teacher, Supervisor, Student
- **Responsive UI**: Works on both desktop and mobile devices
- **Secure login/registration**: Auto-generated user IDs
- **JSON question upload**: Easy question bank management
- **Timed exams**: Auto-submit when time expires
- **Exam security**: Full-screen enforcement, tab switching prevention
- **One-time exam access**: Prevents retakes unless rescheduled
- **Reporting**: Printable exam results and analytics
- **Gamification**: Honor Roll and Leaderboard systems
- **Fatigue-free UI**: Modern, clean interface designed for extended use

### User Role Capabilities

| Role        | Capabilities |
|-------------|--------------|
| Admin       | Full system control, user management, exam scheduling |
| Teacher     | Create exams, upload questions, view results |
| Supervisor  | Monitor active exams, assist students |
| Student     | Take exams, view results and leaderboard |

## Technical Specifications

### Frontend
- **Framework**: React.js (v18+)
- **State Management**: Context API + useReducer
- **Routing**: React Router v6
- **UI Components**: Material-UI (MUI) with custom styling
- **Charts**: Recharts for result visualization
- **PDF Generation**: React-to-PDF for printable reports

### Backend (Mock for offline use)
- **Data Storage**: JSON files with local storage fallback
- **Authentication**: JWT-based mock service
- **API**: Axios with mock service worker for offline development

## Installation & Setup

### Prerequisites
- Node.js (v16+)
- npm (v8+) or yarn
- Git (for version control)

### Installation Steps

1. Clone the repository:
```bash
git clone https://github.com/IamAdedo/Online-Test-Web-App.git
cd online-examination-system
```

2. Install dependencies:
```bash
npm install
# or
yarn install
```

3. Configure the application:
```bash
cp .env.example .env
# Edit the .env file with your local network settings
```

4. Start the development server:
```bash
npm start
# or
yarn start
```

### Deployment for Local Network

1. Build the production version:
```bash
npm run build
# or
yarn build
```

2. Serve the build folder using a local server:
```bash
npm install -g serve
serve -s build -l 3000
```

3. Access the application from other devices on the same network at:
```
http://[your-local-ip]:3000
```

## Project Structure

```
online-examination-system/
├── public/                  # Static files
├── src/
│   ├── assets/              # Images, fonts, etc.
│   ├── components/          # Reusable UI components
│   ├── contexts/            # React contexts
│   ├── hooks/               # Custom hooks
│   ├── pages/               # Application pages
│   │   ├── Admin/           # Admin-specific pages
│   │   ├── Teacher/         # Teacher-specific pages
│   │   ├── Supervisor/      # Supervisor-specific pages
│   │   ├── Student/         # Student-specific pages
│   │   ├── Auth/            # Authentication pages
│   │   └── Shared/          # Shared pages across roles
│   ├── services/            # API/services
│   ├── styles/              # Global styles
│   ├── utils/               # Utility functions
│   ├── App.js               # Main application component
│   └── index.js             # Application entry point
├── .env.example             # Environment variables template
├── .gitignore               # Git ignore file
├── LICENSE                  # Project license
├── package.json             # Project dependencies
└── README.md                # This file
```
