README_clean.md


Resume Matcher
AI-powered resume tailoring and job matching application. Upload a master resume, provide a job description, review AI-generated improvements, and export a tailored resume.

Features
Upload a master resume in PDF or DOCX format

Add a target job description

AI-powered resume tailoring

Resume scoring and keyword highlighting

Identify matched and missing job-description keywords

Generate tailored cover letters

Generate resume-grounded interview preparation

Customize resume sections and layout

Export tailored resumes and cover letters as PDF

Multiple resume templates

Multi-language interface and generated content

How It Works
Upload your master resume.

Paste the job description for the role.

Analyze the resume against the job description.

Review keyword gaps and AI-generated improvements.

Customize the resume content and layout.

Export the final resume as a professional PDF.

Installation
Prerequisites
Tool	Version
Python	3.13+
Node.js	22+
uv	Latest
Quick Start
Backend
cd apps/backend
cp .env.example .env
# Configure your AI provider in .env
uv sync
uv run app
Frontend
Open a second terminal:

cd apps/frontend
npm install
npm run dev
Then open the local URL displayed by the frontend development server.

AI Providers
Resume Matcher uses LiteLLM to support multiple AI providers.

Provider	Type
Ollama	Local
OpenAI	Cloud
Anthropic	Cloud
Google Gemini	Cloud
OpenRouter	Cloud
DeepSeek	Cloud
Groq	Cloud
Provider configuration is controlled through the backend environment configuration.

Docker
The application can also be run with Docker.

docker run --name resume-matcher \
  -p 3000:3000 \
  -v resume-data:/app/backend/data \
  ghcr.io/srbhr/resume-matcher:latest
When running the application through Docker, the app is available on port 3000.

Endpoints
App: http://localhost:3000

API health check: http://localhost:3000/api/v1/health

API documentation: http://localhost:3000/docs

Tech Stack
Component	Technology
Backend	FastAPI, Python, LiteLLM
Frontend	Next.js, React, TypeScript
Database	TinyDB (JSON file storage)
Styling	Tailwind CSS
PDF	Headless Chromium via Playwright
Resume Templates
The application supports multiple resume layouts:

Classic Single Column

Modern Single Column

Classic Two Column

Modern Two Column

Internationalization
The application supports:

English

Spanish

Chinese

Japanese

Brazilian Portuguese

Resume and cover-letter content can also be generated in the selected language.

Project Structure
Resume-Matcher/
├── apps/
│   ├── backend/
│   └── frontend/
├── assets/
├── README.md
└── SETUP.md
Development
Start the backend and frontend separately during local development.

Backend:

cd apps/backend
uv run app
Frontend:

cd apps/frontend
npm run dev
License
This project is released under the Apache 2.0 License.