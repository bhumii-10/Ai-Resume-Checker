# AI Resume Checker

An AI-powered full-stack resume analysis and optimization platform that helps users evaluate, improve, version, and track their resumes through ATS-oriented analysis and generative AI.

## Overview

AI Resume Checker provides an end-to-end workflow for resume optimization. Users can upload a resume, receive an AI-generated analysis with an ATS score, identify missing keywords and improvement areas, rewrite resume content, create new resume versions, and compare changes across versions.

The platform combines a React-based frontend, Node.js/Express backend, MongoDB persistence, and Google Gemini for AI-powered resume analysis and rewriting.

## Key Features

- **Secure Authentication** — JWT-based registration, login, protected routes, profile and password management.
- **Resume Management** — Upload, parse, view, and manage resumes.
- **ATS Analysis** — Generate ATS-oriented scores, identify issues, keywords, strengths, and improvement areas.
- **AI-Powered Rewriting** — Improve resume content using Gemini while preserving version history.
- **Resume Versioning** — Maintain multiple versions with parent-version relationships and independent analysis data.
- **Version Comparison** — Compare two resume versions and identify content changes.
- **Dashboard** — Track ATS scores, resume versions, issues, keywords, and recent activity.
- **Analytics & Insights** — Analyze score trends, common issues, keyword patterns, and resume performance.
- **Activity History** — Track uploads, analyses, and rewrite operations chronologically.

## Tech Stack

### Frontend
- React.js
- Vite
- Tailwind CSS
- Axios

### Backend
- Node.js
- Express.js
- Mongoose
- JWT
- Multer
- Zod

### Database & AI
- MongoDB Atlas
- Google Gemini API

### Development
- Git & GitHub
- Postman
- Nodemon
- VS Code

## Architecture

```text
┌─────────────────────┐
│     React Client    │
│   React + Vite      │
└──────────┬──────────┘
           │ REST API
           ▼
┌─────────────────────┐
│   Express Backend   │
│                     │
│ Routes              │
│ Middleware          │
│ Services            │
│ Models              │
└───────┬───────┬─────┘
        │       │
        ▼       ▼
┌───────────┐ ┌──────────────┐
│ MongoDB   │ │ Gemini API   │
│   Atlas   │ │              │
└───────────┘ └──────────────┘
