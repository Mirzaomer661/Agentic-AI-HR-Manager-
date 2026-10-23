# HR Manager - Resume Parser & Job Matcher

A full-stack web application that parses resumes and matches candidates with job profiles using NLP and skill-based matching.

## Features

- **Resume Upload**: Drag-and-drop upload for PDF and DOCX files
- **Resume Parsing**: Extracts name, contact info, skills, education, experience, and certifications
- **Job Matching**: Matches candidates against predefined job profiles with scoring
- **Dashboard**: View all candidates with search and filter capabilities
- **Job Profile Management**: Add, edit, and delete job profiles

## Tech Stack

- **Frontend**: React + Vite + Tailwind CSS
- **Backend**: Python + FastAPI
- **Resume Parsing**: pdfplumber, python-docx, spaCy
- **Database**: JSON file storage

## Setup Instructions

### Prerequisites

- Python 3.8+
- Node.js 16+
- npm or yarn

### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd HR-Manager/backend
   ```

2. Install Python dependencies:
   ```bash
   pip install fastapi uvicorn python-multipart pdfplumber python-docx spaCy aiofiles
   ```

3. Download spaCy English model:
   ```bash
   python -m spacy download en_core_web_sm
   ```

4. Start the backend server:
   ```bash
   python main.py
   ```

   The API will run at `http://localhost:8000`

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd HR-Manager/frontend
   ```

2. Install npm dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

   The frontend will run at `http://localhost:5173`

### Access the Application

Open your browser and go to `http://localhost:5173`

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/upload-resume` | Upload and parse a resume |
| GET | `/api/candidates` | Get all candidates |
| GET | `/api/candidates/{id}` | Get a specific candidate |
| DELETE | `/api/candidates/{id}` | Delete a candidate |
| GET | `/api/job-profiles` | Get all job profiles |
| POST | `/api/job-profiles` | Create a job profile |
| PUT | `/api/job-profiles/{id}` | Update a job profile |
| DELETE | `/api/job-profiles/{id}` | Delete a job profile |

## Job Profiles Included

1. Frontend Developer
2. Backend Developer
3. Full Stack Developer
4. Data Analyst
5. Data Scientist
6. DevOps Engineer
7. Project Manager
8. HR Coordinator
9. Sales Executive
10. Marketing Specialist
11. QA Engineer
12. Game Developer

## Project Structure

```
HR-Manager/
├── backend/
│   ├── main.py           # FastAPI application
│   ├── parser.py         # Resume parsing logic
│   ├── matcher.py        # Job matching algorithm
│   ├── data/
│   │   └── job_profiles.json
│   └── uploads/          # Uploaded resumes
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── UploadPage.jsx
│   │   │   ├── DashboardPage.jsx
│   │   │   └── JobProfilesPage.jsx
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── package.json
└── README.md
```

## License

MIT