# DevFest Ajah AI Assistant

A secure, scalable full-stack web app built for the "Angular Meets AI" DevFest talk.

## Overview

- **Frontend**: Angular 21 + Ng Zorro
- **Backend**: Node.js + Express + TypeScript  
- **AI**: Google Gemini 3 Pro (via backend)

## Prerequisites

- Node.js 20.x (LTS)
- npm

## Project Structure

```
devfestAjah/
├── client/          # Angular 21 frontend
└── server/          # Node.js/Express backend
```

## Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Daniblueboy/devfestajah-AI.git
   cd devfestajah-AI
   ```

2. **Install dependencies**
   ```bash
   # Backend
   cd server
   npm install
   
   # Frontend
   cd ../client
   npm install
   ```

3. **Environment Variables**
   
   Create `server/.env`:
   ```env
   PORT=3000
   GEMINI_API_KEY=your_api_key_here
   GEMINI_MODEL=gemini-3-pro
   GEMINI_API_BASE_URL=https://generativelanguage.googleapis.com
   ```
   
   Get your API key from: https://makersuite.google.com/app/apikey

## Running Locally

### Backend
```bash
cd server
npm run dev      # Development with hot reload
# or
npm run build && npm start  # Production
```

Server runs on: http://localhost:3000

### Frontend
```bash
cd client
npm start
```

Frontend runs on: http://localhost:4200

## Features

- **Dashboard**: Overview and quick stats
- **AI Chat**: Conversational AI powered by Gemini 3 Pro
- **Code Helper**: Get AI suggestions and improvements for code snippets

## Deployment

### Frontend (Netlify)
- Already configured with `netlify.toml`
- See `client/README.md` for details

### Backend (Render)
- Configured with `render.yaml`
- See `server/DEPLOYMENT.md` for step-by-step guide
- **Important**: Set `GEMINI_API_KEY` in Render environment variables

## Tech Stack

### Frontend
- Angular 21
- Ng Zorro (Ant Design)
- RxJS
- TypeScript 5.9

### Backend
- Node.js 20.x
- Express 5
- Google Generative AI (Gemini 3 Pro)
- TypeScript 5.9
- Zod (validation)
- Helmet (security)

## API Endpoints

- `POST /api/chat` - Chat with AI
- `POST /api/code-helper` - Get code suggestions
- `GET /health` - Health check

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## License

ISC

## Author

Built for DevFest Ajah 2025 - "Angular Meets AI" Talk
