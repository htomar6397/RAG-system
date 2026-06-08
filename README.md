# RAG System - Retrieval Augmented Generation

A comprehensive Retrieval-Augmented Generation (RAG) system combining AI-powered search with a modern web interface. This project integrates Python-based AI services with a Node.js backend and React frontend for intelligent document retrieval and analysis.

---

## 🚀 Features

### AI Service (Python)
- **Pipeline Processing**: Advanced document chunking and processing pipeline
- **Embeddings**: State-of-the-art embeddings generation for semantic search
- **Vector Store**: Efficient vector database for similarity search
- **Code Indexing**: Specialized indexing for code repositories
- **LLM Integration**: Large Language Model integration for intelligent responses
- **Comprehensive Tests**: Full unit test coverage for pipeline modules

### Backend (Node.js/Express)
- **RESTful API**: Clean API endpoints for all operations
- **Authentication**: Secure user authentication and authorization
- **Document Management**: Upload, process, and manage documents
- **Search API**: Fast full-text and semantic search capabilities
- **Analytics**: Detailed analytics and usage tracking
- **TypeScript**: Fully typed backend for reliability

### Frontend (React)
- **Modern UI**: React with TypeScript for type-safe components
- **Search Interface**: Intuitive search functionality
- **Upload Management**: Easy document upload and management
- **Authentication UI**: Secure login interface
- **Responsive Design**: Works seamlessly on desktop and mobile
- **Vite Build Tool**: Fast development and production builds

---

## 📋 Project Structure

```
rag-system/
├── ai-service/                    # Python AI service
│   ├── app/
│   │   ├── __init__.py
│   │   ├── config.py             # Configuration
│   │   ├── main.py               # Entry point
│   │   ├── models.py             # Data models
│   │   ├── pipeline.py           # Processing pipeline
│   │   ├── seed.py               # Data seeding
│   │   └── services/             # Core services
│   │       ├── chunking.py       # Document chunking
│   │       ├── code_index.py     # Code indexing
│   │       ├── codes.py          # Code utilities
│   │       ├── embeddings.py     # Embeddings generation
│   │       ├── llm.py            # LLM integration
│   │       └── vector_store.py   # Vector storage
│   ├── tests/
│   │   ├── __init__.py
│   │   └── test_pipeline.py      # Pipeline tests
│   ├── Dockerfile                # Docker configuration
│   └── requirements.txt           # Python dependencies
│
├── backend/                       # Node.js backend
│   ├── src/
│   │   ├── index.ts              # Entry point
│   │   ├── config.ts             # Configuration
│   │   ├── auth.ts               # Authentication logic
│   │   ├── aiClient.ts           # AI service client
│   │   ├── store.ts              # Data store
│   │   ├── types.ts              # TypeScript types
│   │   └── routes/               # API routes
│   │       ├── auth.ts           # Auth endpoints
│   │       ├── search.ts         # Search endpoints
│   │       ├── ask.ts            # Query endpoints
│   │       ├── documents.ts      # Document management
│   │       └── analytics.ts      # Analytics endpoints
│   ├── frontend/                 # React frontend
│   │   ├── src/
│   │   │   ├── main.tsx          # Entry point
│   │   │   ├── App.tsx           # Main app component
│   │   │   ├── api.ts            # API client
│   │   │   ├── styles.css        # Global styles
│   │   │   ├── vite-env.d.ts     # Vite types
│   │   │   └── components/       # React components
│   │   │       ├── Login.tsx      # Login component
│   │   │       ├── Search.tsx     # Search component
│   │   │       └── Upload.tsx     # Upload component
│   │   ├── index.html            # HTML template
│   │   ├── package.json          # Frontend dependencies
│   │   ├── tsconfig.json         # TypeScript config
│   │   └── vite.config.ts        # Vite configuration
│   ├── Dockerfile                # Backend Docker config
│   ├── package.json              # Dependencies
│   ├── tsconfig.json             # TypeScript config
│   └── package-lock.json         # Locked dependencies
│
├── docker-compose.yml            # Multi-container setup
├── prd.md                         # Product Requirements
├── CHANGELOG.md                   # Version history
├── .gitignore                     # Git ignore rules
├── .env.example                   # Environment variables template
└── .vscode/                       # VS Code settings
```

---

## 🛠 Tech Stack

### Backend
- **Runtime**: Node.js
- **Framework**: Express.js
- **Language**: TypeScript
- **API**: RESTful

### Frontend
- **Library**: React
- **Language**: TypeScript
- **Build Tool**: Vite
- **Styling**: CSS

### AI Service
- **Language**: Python
- **Key Libraries**:
  - Document processing and chunking
  - Vector embeddings generation
  - Vector database operations
  - LLM integration

### Infrastructure
- **Containerization**: Docker
- **Orchestration**: Docker Compose

---

## 📦 Installation

### Prerequisites
- Docker & Docker Compose
- Node.js 18+ (for local development)
- Python 3.9+ (for AI service development)

### Quick Start with Docker

```bash
# Clone the repository
git clone https://github.com/htomar6397/RAG-system.git
cd rag-system

# Build and run with Docker Compose
docker-compose up --build
```

The application will be available at:
- Frontend: http://localhost:3000
- Backend: http://localhost:5000
- AI Service: http://localhost:8000

### Local Development

#### Backend Setup
```bash
cd backend
npm install
npm run dev
```

#### Frontend Setup
```bash
cd backend/frontend
npm install
npm run dev
```

#### AI Service Setup
```bash
cd ai-service
pip install -r requirements.txt
python -m app.main
```

---

## 🔌 API Endpoints

### Authentication
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `POST /api/auth/signup` - User registration

### Search
- `POST /api/search/query` - Full-text + semantic search
- `GET /api/search/history` - Search history

### Documents
- `POST /api/documents/upload` - Upload new documents
- `GET /api/documents/list` - List all documents
- `DELETE /api/documents/:id` - Delete document

### Ask/Query
- `POST /api/ask/query` - Ask questions about documents
- `GET /api/ask/history` - Query history

### Analytics
- `GET /api/analytics/stats` - System statistics
- `GET /api/analytics/usage` - Usage analytics

---

## 🧪 Testing

### Run Pipeline Tests
```bash
cd ai-service
pytest tests/
```

### Test Coverage
- Unit tests for pipeline modules
- Integration tests for API endpoints
- E2E tests for full workflows

---

## 📝 Environment Variables

Create `.env` file from `.env.example`:

```env
# Database
DATABASE_URL=postgresql://user:password@localhost/ragdb

# AI Service
AI_SERVICE_URL=http://ai-service:8000

# JWT
JWT_SECRET=your-secret-key
JWT_EXPIRY=24h

# Frontend
REACT_APP_API_URL=http://localhost:5000
```

---

## 🚀 Deployment

### Docker Deployment
```bash
docker-compose -f docker-compose.yml up -d
```

### Environment-Specific Configs
- Development: `docker-compose.yml`
- Production: Create `docker-compose.prod.yml`

---

## 📊 Project Timeline

- **June 2-8, 2026**: Initial project development
  - Project structure and core configs
  - AI service initialization
  - Backend setup
  - Frontend implementation
  - API routes and integration
  - Testing and documentation

---

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'feat: add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

---

## 📄 License

This project is licensed under the MIT License - see LICENSE file for details.

---

## 👤 Author

**Mayank Tomar**
- Email: htomar6397@gmail.com
- GitHub: [@htomar6397](https://github.com/htomar6397)

---

## 🔗 Links

- [GitHub Repository](https://github.com/htomar6397/RAG-system)
- [Documentation](./prd.md)
- [Changelog](./CHANGELOG.md)

---

## ⚡ Quick Commands

```bash
# Start all services
docker-compose up -d

# View logs
docker-compose logs -f

# Stop services
docker-compose down

# Rebuild containers
docker-compose up -d --build

# Run tests
docker-compose exec ai-service pytest tests/

# Access backend
docker-compose exec backend bash

# Access AI service
docker-compose exec ai-service bash
```

---

## 🐛 Troubleshooting

### Port Already in Use
```bash
# Find process using port
lsof -i :3000
# Kill it
kill -9 <PID>
```

### Docker Build Issues
```bash
# Clear cache and rebuild
docker-compose build --no-cache
```

### Database Connection Issues
- Verify DATABASE_URL in .env
- Ensure database service is running
- Check network connectivity

---

## 📞 Support

For issues, questions, or contributions:
- Open an Issue on GitHub
- Contact: htomar6397@gmail.com

---

**Last Updated**: June 10, 2026
