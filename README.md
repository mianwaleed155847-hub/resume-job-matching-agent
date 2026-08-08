# Resume / Job-Matching Agent

An AI agent built with **CrewAI** that automatically parses a resume and compares it against a job description — returning a match score, matching skills, missing requirements, and a recommendation.

## Features
- **Resume Parser Tool** — extracts Skills, Experience, and Education from resume text/PDF
- **Job Match Comparator Tool** — compares parsed resume against a job description
- Single CrewAI agent (`Resume Matching Specialist`) orchestrating both tools
- Match report includes: score out of 100, matching points, missing points, recommendation
- Streamlit web UI for interactive use
- Powered by Groq (`gpt-oss-120b`) via LiteLLM
- Deployed from Google Colab using ngrok tunnel

## Tech Stack
- CrewAI + CrewAI Tools
- LiteLLM (Groq backend)
- Streamlit
- pypdf (PDF resume parsing)
- pyngrok (public URL tunneling)

## How It Works
1. User provides a resume (text/PDF) and a job description
2. `ResumeParserTool` extracts structured info from the resume
3. `JobMatchComparatorTool` compares it against the job description
4. Agent returns a full match report with score, gaps, and suggestions

## Setup
```bash
pip install -r requirements.txt
```

Set your API keys as environment variables / Streamlit secrets:
- `GROQ_API_KEY`
- `NGROK_AUTHTOKEN` (only needed for Colab tunnel deployment)

## Run
```bash
streamlit run app.py
```

## Project Status
Part of an ongoing AI Agents portfolio — built as part of a broader CrewAI/LangGraph multi-agent project series.
