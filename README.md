# Mock API AI System

Platform for generating, hosting, and testing dynamic mock REST APIs with persistent CRUD operations and an interactive playground.

---

## System Architecture

Mock API AI consists of a frontend application and a backend API working together.

The frontend is used to generate APIs, test endpoints, and manage request data.

The backend handles AI-based schema generation, validation, dynamic CRUD operations, and PostgreSQL data storage.

### Mock API AI Frontend

React-based dashboard and API playground for generating APIs, editing request payloads, and testing dynamic CRUD endpoints.

### Mock API AI Backend

Node.js and Express backend responsible for AI-powered schema generation, runtime validation, dynamic CRUD operations, and PostgreSQL persistence.

---

## Repository Structure

| Repository | Description | Link |
|---|---|---|
| **Mock API AI Frontend** | React dashboard and API playground | [View Repository](https://github.com/sn0914r/mock-api-ai-frontend) |
| **Mock API AI Backend** | Express.js backend and dynamic API engine | [View Repository](https://github.com/sn0914r/mock-api-ai-backend) |

---

## Live Deployments

- **Frontend:** [mock-api-ai.pages.dev](https://mock-api-ai.pages.dev/)
- **Backend API:** [mock-api-ai-backend](https://site--mock-api-ai-backend--gxd2ltpdfxvn.code.run/health)

---

## Core Features

- Generate mock REST APIs from natural language prompts
- Dynamic schema and mock data generation using Groq LLM
- Persistent CRUD operations using PostgreSQL JSONB
- Interactive API playground for testing endpoints
- Runtime payload validation for dynamic APIs
- Syntax-highlighted API responses
- Dark and light theme support

---

## System Flow

### API Generation Flow

- User submits a prompt from the frontend dashboard
- Backend sends the prompt to Groq LLM for schema and mock data generation
- Generated API metadata and records are stored in PostgreSQL
- Backend returns a unique API endpoint for CRUD operations

### Dynamic API Request Flow

- Requests are made to `/api/:apiId/:route`
- Backend retrieves the stored schema for validation
- Incoming payloads are validated at runtime
- PostgreSQL JSONB records are updated and returned in the response

### Playground Workflow

- Users select an API from the dashboard
- Request payloads can be edited directly in the playground
- Responses are displayed with syntax highlighting and copy support

---

## Tech Stack

### Frontend

- React
- Vite
- TanStack Query
- React Router
- React Hook Form
- Bootstrap
- Emotion

### Backend

- Node.js
- Express.js
- TypeScript
- PostgreSQL
- pg

### AI Integration

- Groq API
- Llama 3.3 70B Versatile

### Validation & Security

- Zod
- Helmet
- CORS
- Custom runtime payload validation

### Deployment

- Cloudflare Pages (Frontend Hosting)
- Northflank (Backend Hosting)
- Neon PostgreSQL (Database)

---

## Project Structure

The Mock API AI system is split into two independent repositories:

- `mock-api-ai-frontend` — Dashboard and interactive API playground
- `mock-api-ai-backend` — Dynamic API generation and CRUD backend

Both applications communicate through the backend API.

---

## Environment Setup

### Backend

Requires:
- PostgreSQL database
- Groq API key

### Frontend

Requires:
- Backend API URL

---

## Security

- Dynamic API isolation using UUID-based routing
- Runtime payload validation for `POST`, `PUT`, and `PATCH`
- Centralized error handling middleware
- Structured validation and error responses
- Secure HTTP headers using Helmet
- Safe production error handling without stack trace exposure

---

## Documentation

For detailed information about each part of the system:

- [Mock API AI Frontend Documentation](https://github.com/sn0914r/mock-api-ai-frontend)
- [Mock API AI Backend Documentation](https://github.com/sn0914r/mock-api-ai-backend)
