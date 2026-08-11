# 🚀 AI Resume Checker

> **AI-powered resume analysis, ATS optimization, rewriting, versioning, and insights — all in one platform.**

AI Resume Checker is a full-stack AI-powered platform designed to help users analyze, improve, and manage their resumes. It combines ATS-oriented scoring, AI-generated recommendations, resume rewriting, version control, analytics, and activity tracking into a single modern web application.

The platform uses **React + Vite** on the frontend, **Node.js + Express** on the backend, **MongoDB Atlas** for persistence, and **Google Gemini** for intelligent resume analysis and rewriting.

---

## 🌐 Live Demo

### Frontend
🔗 https://ai-resume-checker-frontend-nine.vercel.app

### Backend API
🔗 https://ai-resume-checker-umber-two.vercel.app

> The backend root endpoint intentionally returns `Route GET / not found` because the API does not expose a homepage route. The backend REST endpoints are consumed directly by the frontend.

---

## ✨ Features

### 🔐 Authentication
- Secure user registration and login
- JWT-based authentication
- HTTP cookie-based sessions
- Protected API routes
- Profile management
- Password management
- Authentication-aware frontend routing

### 📄 Resume Management
- Upload resumes in PDF format
- Server-side PDF parsing
- Resume text extraction
- Resume storage and management
- View previously uploaded resumes
- Track resume activity

### 🎯 ATS Resume Analysis
- AI-powered ATS score generation
- Resume strengths and weaknesses
- Missing keyword identification
- Resume issue detection
- Improvement recommendations
- Job-readiness insights
- Actionable optimization suggestions

### 🤖 AI-Powered Resume Rewriting
- AI-assisted resume improvement
- Rewrite weak resume content
- Generate stronger resume bullets
- Improve clarity and impact
- Preserve resume context while improving wording

### 🧬 Resume Versioning
- Create multiple resume versions
- Maintain parent-child version relationships
- Track changes between versions
- Store independent analysis results
- Maintain a history of resume improvements

### 📊 Dashboard
- Overall ATS score
- Resume activity
- Resume versions
- Detected issues
- Keywords
- Recent activity
- Quick access to resume analysis

### 📈 Analytics & Insights
- ATS score trends
- Resume performance tracking
- Common resume issues
- Keyword patterns
- Historical analysis
- Resume improvement insights

### 🕒 Activity History
Track important resume operations such as:

- Resume uploads
- Resume analysis
- AI rewriting
- Version creation
- Resume updates

---

# 🛠️ Tech Stack

## Frontend

| Technology | Purpose |
|------------|---------|
| React.js | Frontend UI |
| Vite | Development & production build |
| Tailwind CSS | Styling |
| Axios | API communication |
| React Router | Client-side routing |

## Backend

| Technology | Purpose |
|------------|---------|
| Node.js | Runtime |
| Express.js | REST API |
| Mongoose | MongoDB ODM |
| JWT | Authentication |
| Cookie-based Sessions | Secure authentication |
| Multer | File uploads |
| Zod | Request validation |
| pdf-parse | PDF text extraction |
| @napi-rs/canvas | PDF parsing support |

## Database & AI

| Technology | Purpose |
|------------|---------|
| MongoDB Atlas | Database |
| Google Gemini API | AI resume analysis & rewriting |

## Development & Deployment

- Git
- GitHub
- VS Code
- Postman
- Nodemon
- Vercel

---

# 🏗️ System Architecture

```text
                         ┌──────────────────────────┐
                         │        User / Browser    │
                         └────────────┬─────────────┘
                                      │
                                      ▼
                         ┌──────────────────────────┐
                         │      React Frontend      │
                         │       Vite + Tailwind    │
                         │                          │
                         │  Dashboard               │
                         │  Resume Management       │
                         │  Analytics               │
                         │  Versioning              │
                         │  Authentication          │
                         └────────────┬─────────────┘
                                      │
                                  REST API
                                      │
                                      ▼
                         ┌──────────────────────────┐
                         │    Node.js + Express     │
                         │        Backend           │
                         │                          │
                         │  Authentication          │
                         │  Resume Routes           │
                         │  Dashboard Routes        │
                         │  Analytics Routes        │
                         │  History Routes          │
                         │  Resume Services         │
                         └───────┬──────────┬───────┘
                                 │          │
                    ┌────────────┘          └─────────────┐
                    ▼                                    ▼
          ┌──────────────────┐                 ┌──────────────────┐
          │   MongoDB Atlas  │                 │   Google Gemini  │
          │                  │                 │                  │
          │ Users            │                 │ AI Analysis      │
          │ Resumes          │                 │ AI Rewriting     │
          │ Versions         │                 │ Recommendations  │
          │ Activity         │                 │ ATS Insights     │
          └──────────────────┘                 └──────────────────┘
