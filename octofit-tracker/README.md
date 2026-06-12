# OctoFit Tracker

A modern multi-tier fitness tracking application built with GitHub Copilot agent mode.

## Project Structure

```
octofit-tracker/
├── frontend/          # React 19 + Vite frontend
│   ├── src/
│   ├── package.json
│   ├── vite.config.ts
│   └── tsconfig.json
├── backend/           # Node.js + Express + TypeScript backend
│   ├── src/
│   ├── package.json
│   ├── tsconfig.json
│   └── .env.example
└── README.md
```

## Technology Stack

### Frontend
- **React 19** - UI library
- **Vite** - Build tool and dev server (port 5173)
- **TypeScript** - Type safety

### Backend
- **Node.js + Express** - Server framework
- **TypeScript** - Type safety
- **Mongoose** - MongoDB ODM
- **CORS** - Cross-origin resource sharing (port 8000)

### Database
- **MongoDB** - NoSQL database (port 27017)

## Setup Instructions

### Prerequisites
- Node.js 18+ and npm
- MongoDB running locally or a connection string

### Frontend Setup

```bash
cd octofit-tracker/frontend
npm install
npm run dev
```

Frontend will be available at `http://localhost:5173`

### Backend Setup

```bash
cd octofit-tracker/backend
npm install

# Create .env file from template
cp .env.example .env

# Update .env with your MongoDB URI if needed
npm run dev
```

Backend will be available at `http://localhost:8000`

## Available Ports

- **Frontend**: 5173
- **Backend**: 8000
- **MongoDB**: 27017

## Scripts

### Frontend
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build

### Backend
- `npm run dev` - Start development server with ts-node
- `npm run build` - Compile TypeScript to JavaScript
- `npm start` - Run compiled backend
- `npm run lint` - Run ESLint

## Health Check

Once the backend is running, test it with:

```bash
curl http://localhost:8000/api/health
```

Expected response:
```json
{
  "status": "OK",
  "message": "OctoFit Tracker Backend is running"
}
```

## Next Steps

1. Define MongoDB schemas and models
2. Create API routes for fitness tracking
3. Build React components for the frontend
4. Integrate frontend with backend API
5. Deploy to production
