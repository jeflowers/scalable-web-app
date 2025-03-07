# Scalable Web Application

A modular, scalable web application with Python/FastAPI backend, TypeScript/React frontend, and configurable infrastructure.

## Architecture

This application follows a clean architecture approach with the following key components:

- **Backend**: Python with FastAPI
- **Frontend**: TypeScript with React
- **Database**: Configurable through abstraction
- **Email Service**: Configurable through abstraction
- **Authentication**: Multiple swappable mechanisms
- **Deployment**: Options for serverless, containers, or Kubernetes

## Project Structure

```
.
├── backend/            # FastAPI application
│   ├── core/           # Core business logic
│   ├── api/            # API endpoints
│   ├── adapters/       # Database and external service adapters
│   ├── domain/         # Domain models
│   └── tests/          # Backend tests
├── frontend/          # React/TypeScript application
│   ├── src/            # Source code
│   ├── public/         # Static files
│   └── tests/          # Frontend tests
├── infrastructure/    # Deployment configurations
│   ├── serverless/     # Serverless deployment
│   ├── container/      # Container deployment
│   └── kubernetes/     # Kubernetes deployment
└── docs/              # Project documentation
```

## Getting Started

### Backend Setup

```bash
# Navigate to backend directory
cd backend

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run development server
uvicorn main:app --reload
```

### Frontend Setup

```bash
# Navigate to frontend directory
cd frontend

# Install dependencies
npm install

# Start development server
npm start
```

## Development

- Backend API is available at http://localhost:8000/api/v1
- Frontend development server runs at http://localhost:3000
- API documentation is available at http://localhost:8000/api/v1/docs

## Deployment

The application can be deployed using one of the following methods:

1. **Serverless**: Best for variable workloads and minimal DevOps
2. **Container**: Better for consistent workloads with more control
3. **Kubernetes**: Ideal for complex deployments with multiple services

See the `/infrastructure` directory for specific deployment configurations.
