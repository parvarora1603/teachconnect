# TeachConnect Backend

This is the backend for TeachConnect, a Flutter-based teacher-student education app.

## Features

- Authentication (login/register)
- Chatbot support using Google Gemini API
- Assignment creation and submission
- MCQ auto-grading
- Written assignment review
- Notes saving system

## Tech Stack

- Node.js
- Firebase (Firestore, Auth, Storage)
- Google Gemini API
- Vercel for deployment

## Deployment Steps

1. Push this code to a GitHub repository
2. Go to [Vercel](https://vercel.com) and connect your GitHub repository
3. Set up the following environment variables in Vercel:
   - FIREBASE_API_KEY
   - FIREBASE_AUTH_DOMAIN
   - FIREBASE_PROJECT_ID
   - FIREBASE_STORAGE_BUCKET
   - FIREBASE_MESSAGING_SENDER_ID
   - FIREBASE_APP_ID
   - GEMINI_API_KEY
4. Deploy the project

## API Endpoints

### Authentication
- POST /api/auth/login
- POST /api/auth/register

### Chatbot
- POST /api/chatbot/ask

### Assignments
- POST /api/assignments/create
- POST /api/assignments/submitMCQ
- POST /api/assignments/submitWritten
- GET /api/assignments/getStudentAssignments
- GET /api/assignments/getTeacherAssignments

### Reports
- GET /api/report/mcqResults
- GET /api/report/writtenResults
- POST /api/report/writtenResults (for submitting reviews)

### Notes
- POST /api/notes/saveNote
- GET /api/notes/getNotes

## Flutter Integration

To connect your Flutter frontend to this backend:

1. Use the `http` package to make API calls
2. Use Firebase Auth for authentication
3. Update your Flutter app's Firebase configuration to match the backend

