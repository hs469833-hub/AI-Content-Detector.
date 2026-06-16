# AI Content Detector Pro SaaS

A production-ready full-stack SaaS application for AI content detection, text humanization, and writing analysis.

## Features
- **Advanced AI Detection**: Sentence-level analysis for Images, Videos, Audio, PDF, DOCX, and TXT.
- **AI Writing Suite**: Humanize AI text, check readability, and SEO scores.
- **Complete Auth System**: JWT Access/Refresh tokens, RBAC, and secure session management.
- **User Management**: Profile image uploads, persistent settings, and account management.
- **Admin Panel**: System-wide analytics, user management, and health monitoring.
- **Security**: Rate limiting, CORS protection, and secure file handling.

## Tech Stack
- **Frontend**: React.js (Vite), Tailwind CSS, Lucide Icons, Recharts, Framer Motion.
- **Backend**: FastAPI (Python 3.13), SQLAlchemy, PostgreSQL (recommended), SlowAPI.
- **AI Integration**: Modular support for OpenAI (GPT-3.5/4) and Google Gemini.

## Installation

### Backend
1. `cd backend`
2. `python -m venv .venv`
3. `source .venv/bin/activate` (Windows: `.venv\Scripts\activate`)
4. `pip install -r requirements.txt`
5. Configure `.env` (see `.env.example`)
6. `uvicorn main:app --reload`

### Frontend
1. `cd frontend`
2. `npm install`
3. Configure `.env`
4. `npm run dev`

## Environment Variables (.env)
### Backend
```env
PROJECT_NAME="AI Content Detector Pro"
SECRET_KEY="your-secret-key"
DATABASE_URL="sqlite:///./sql_app.db" # Or PostgreSQL URL
OPENAI_API_KEY="sk-..."
GEMINI_API_KEY="AIza..."
```

### Frontend
```env
VITE_API_URL="/api/v1"
```

## Project Structure
```
.
├── backend/
│   ├── app/
│   │   ├── api/          # API endpoints
│   │   ├── core/         # Configuration and security
│   │   ├── db/           # Database session and base model
│   │   ├── models/       # SQLAlchemy models
│   │   ├── schemas/      # Pydantic schemas
│   │   ├── services/     # Mock detection logic
│   │   └── uploads/      # Storage for uploaded files
│   ├── main.py           # Entry point
│   └── requirements.txt  # Backend dependencies
├── frontend/
│   ├── src/
│   │   ├── components/   # Reusable UI components
│   │   ├── context/      # Auth context
│   │   ├── pages/        # Page components
│   │   ├── services/     # API services
│   │   └── App.jsx       # Routing
│   ├── tailwind.config.js
│   └── package.json      # Frontend dependencies
└── README.md
```

## Setup and Installation

### Backend Setup
1. Navigate to the backend directory:
   ```bash
   cd backend
   ```
2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the backend server:
   ```bash
   uvicorn main:app --reload
   ```
   The API will be available at `http://localhost:8000`.

### Frontend Setup
1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Run the development server:
   ```bash
   npm run dev
   ```
   The frontend will be available at `http://localhost:3000`.

## API Documentation
Once the backend is running, you can access the interactive Swagger UI at:
`http://localhost:8000/docs`

## License
MIT
