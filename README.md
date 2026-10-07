# HireLens — AI Recruitment MVP

An independently developed recruitment MVP by **Kubanychbek Duishekeev**.

HireLens combines vacancy and candidate management, AI-assisted
interview workflows, an HR dashboard and reporting.

> **Source code is private.**
> This repository contains portfolio documentation only.
> The previous test deployment is currently offline.

## Project Overview

HireLens was developed to bring recruitment workflows into one application:

- Managing vacancies and candidate applications
- Supporting interview workflows with AI integrations
- Organizing candidate review through an HR dashboard
- Exporting information for further human review

AI output is decision support. The project is not presented as a
validated replacement for human hiring decisions.

## My Contribution

I independently developed the MVP, including its backend,
frontend and external-service integrations.

I deployed a temporary instance to a **Contabo VPS** and tested
the application there for one month. That deployment is no longer online.

**Development period:** 1 June–26 August 2026.

## Features Implemented in the Source

### Recruitment Workflows

- Vacancy and candidate management
- Team-related workflows
- Candidate application and interview flows
- HR dashboard and Kanban views
- Analytics and reporting

### AI and Integrations

- Anthropic Claude and Groq API integrations
- Provider retry and fallback logic
- Whisper speech-to-text integration through Groq
- FFmpeg media processing
- Google Calendar integration
- Notification modules

### Reporting and Access

- PDF and Excel report generation
- JWT authentication
- Role-based access controls
- API-key and signed-webhook mechanisms
- Rate limiting and audit logging

These features are described from the supplied source archive.
Their presence is not a claim that every scenario has been validated.

## Technology Stack

| Layer | Technologies |
| :--- | :--- |
| Backend | Python, FastAPI, Pydantic |
| Database | PostgreSQL, SQLAlchemy, Alembic |
| Frontend | React 18, Vite, Tailwind CSS, JavaScript/JSX |
| AI providers | Anthropic and Groq Python SDKs |
| Speech and media | Whisper through Groq, FFmpeg |
| Reports | ReportLab, openpyxl |
| Deployment | Docker, Docker Compose |
| Testing | pytest, Vitest |
| Pipeline configuration | GitLab CI |

The archived implementation uses provider SDKs directly.
LangChain and LangGraph are not dependencies of this version.

## Architecture

```text
React / Vite frontend
          |
          v
     FastAPI backend
          |
          +---- PostgreSQL
          |     SQLAlchemy / Alembic
          |
          +---- Anthropic / Groq APIs
          |
          +---- Speech and media processing
          |
          +---- Calendar / notifications
          |
          +---- PDF / Excel reporting
```

## Typical Workflow

1. An HR user creates a vacancy.
2. A candidate submits an application and enters an interview workflow.
3. AI integrations assist with interview processing and analysis.
4. HR reviews the available information.
5. Candidate status is managed through the dashboard.
6. Reports can be exported for further review.

## Source Inventory

Static analysis of the supplied archive identified:

| Item | Count |
| :--- | ---: |
| API route decorator declarations | 122 |
| Backend test functions in test modules | 224 |
| Alembic migration files | 28 |

These numbers describe code inventory:

- Route declarations are not necessarily unique or mounted endpoints.
- Test functions are not a count of successfully passed tests.
- No test-coverage percentage or performance result is claimed.

The application and test suites were not executed during the
portfolio documentation review.

## Project Status and Limitations

**Status:** MVP with private source code; currently offline.

Further validation is needed for:

- Authentication and object-level access controls
- Deployment hardening and load behavior
- External-provider failure handling
- LLM output quality and scoring validity
- Fairness and appropriate use in recruitment
- Privacy and retention of applicant information

Subscription and billing-related modules do not establish the
presence of a working payment gateway.

No commercial customer count, revenue, hiring-accuracy score
or measured performance improvement is claimed.

## Source Availability

Application code, credentials, databases, applicant documents
and interview recordings are not included in this repository.

There are no public installation instructions because the
application source is private.

## Author and Contact

**Kubanychbek Duishekeev**  
Python Backend & AI Developer · Bishkek, Kyrgyzstan

[GitHub](https://github.com/minbaevv) ·
[LinkedIn](https://www.linkedin.com/in/kubanychbek-duishekeev-7b9872427/) ·
[Telegram](https://t.me/d_kubanychbek) ·
[Gmail](mailto:duishekeevkubanychbek@gmail.com)
