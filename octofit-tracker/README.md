# OctoFit Tracker

A modern multi-tier fitness tracking application built with React 19, Node.js/Express, and MongoDB.

## Project Structure

```
octofit-tracker/
├── frontend/          # React 19 + Vite application
├── backend/           # Node.js + Express + TypeScript API
└── docker-compose.yml # Service orchestration
```

## Services & Ports

| Service  | Port  | URL                       | Technology                |
|----------|-------|---------------------------|---------------------------|
| Frontend | 5173  | http://localhost:5173     | React 19 + Vite           |
| Backend  | 8000  | http://localhost:8000     | Express + TypeScript      |
| MongoDB  | 27017 | mongodb://localhost:27017 | MongoDB                   |

## Quick Start

### Prerequisites
- Node.js >= 18.0.0
- npm >= 10.0.0
- Docker and Docker Compose (optional, for MongoDB)

### Installation

1. **Install Frontend Dependencies**
```bash
cd frontend
npm install
```

2. **Install Backend Dependencies**
```bash
cd ../backend
npm install
```

### Running the Application

#### Option 1: Using npm scripts

**Start Backend (Terminal 1)**
```bash
cd backend
npm run dev
```

**Start Frontend (Terminal 2)**
```bash
cd frontend
npm run dev
```

**Start MongoDB (Terminal 3)**
```bash
docker-compose up mongodb
```

#### Option 2: Using Docker Compose

```bash
docker-compose up
```

This will start all services (frontend, backend, and MongoDB) simultaneously.

## Environment Variables

### Backend (.env)

```env
PORT=8000
NODE_ENV=development
MONGODB_URI=mongodb://localhost:27017/octofit-tracker
MONGODB_PORT=27017
FRONTEND_PORT=5173
FRONTEND_URL=http://localhost:5173
CORS_ORIGIN=http://localhost:5173
```

## Available Scripts

### Frontend

```bash
npm run dev      # Start development server (Vite)
npm run build    # Build for production
npm run preview  # Preview production build
```

### Backend

```bash
npm run dev      # Start development server with ts-node
npm run build    # Compile TypeScript to JavaScript
npm run start    # Start compiled server
npm run lint     # Run ESLint
npm run format   # Format code with Prettier
```

## API Endpoints

### Health Check
- `GET /api/health` - Server health status

## Technology Stack

### Frontend
- **React** 19 - UI framework
- **Vite** - Build tool and dev server
- **Node.js** - JavaScript runtime

### Backend
- **Node.js** - JavaScript runtime
- **Express** - Web framework
- **TypeScript** - Type-safe JavaScript
- **Mongoose** - MongoDB object modeling
- **CORS** - Cross-Origin Resource Sharing
- **dotenv** - Environment variable management

### Database
- **MongoDB** - NoSQL database

## Development Guidelines

### Code Style
- Use TypeScript for type safety
- Follow ESLint rules
- Format with Prettier before committing

### Frontend Conventions
- Use functional components with hooks
- Keep components modular and reusable

### Backend Conventions
- Use TypeScript strict mode
- Follow RESTful API design patterns
- Use Mongoose schemas for data validation

## Contributing

1. Create a feature branch from `main`
2. Make your changes
3. Test thoroughly
4. Submit a pull request

## License

MIT
