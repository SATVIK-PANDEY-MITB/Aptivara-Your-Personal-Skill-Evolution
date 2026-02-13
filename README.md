# Aptivara - Gamified Skill Tracker with AI Recommendations

A gamified skill tracking platform that helps you master new abilities through XP rewards, daily streaks, focus timers, and AI-powered learning recommendations.

## Features

- **Gamification System** - Earn XP, level up, and track your progress
- **Daily Streaks** - Build consistency with streak tracking
- **Activity Heatmap** - Visualize your learning patterns (90-day view)
- **Skill Categories** - Organize skills by Technology, Language, Music, Art, Sports, Business, Science, and Soft Skills
- **Focus Timer** - Pomodoro-style timers (25/45/60 min sessions)
- **AI Coach** - Get personalized learning recommendations powered by OpenAI
- **Leaderboard** - Compete with other users
- **Weak Areas Detection** - Identifies skills that need attention

## Tech Stack

**Backend:**
- FastAPI
- SQLAlchemy + SQLite
- JWT Authentication
- OpenAI API

**Frontend:**
- React 18
- React Router DOM
- Vite

## Setup

### Backend

```bash
cd backend
python -m venv venv
venv\Scripts\activate  # Windows
pip install -r requirements.txt
uvicorn main:app --reload
```

### Frontend

```bash
cd frontend
npm install
npm run dev
```

### Environment Variables

Create a `.env` file in the `backend/` folder:

```
SECRET_KEY=your-secret-key-here
OPENAI_API_KEY=your-openai-api-key
```

## API Endpoints

- `POST /auth/register` - Register new user
- `POST /auth/login` - Login and get JWT token
- `GET /skills/` - Get all skills
- `POST /skills/` - Create new skill
- `GET /tasks/` - Get all tasks
- `POST /tasks/` - Create new task
- `POST /tasks/{id}/complete` - Complete task and earn XP
- `GET /dashboard/user-stats` - Get user statistics
- `GET /dashboard/activity-heatmap` - Get activity heatmap data
- `GET /dashboard/leaderboard` - Get top users
- `GET /dashboard/weak-areas` - Get skills needing attention
- `GET /dashboard/ai-recommendation` - Get AI learning tips

## License

MIT
