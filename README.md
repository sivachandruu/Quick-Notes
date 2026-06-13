# ◈ QuickNotes

A full-stack single-page note-taking application.  
**Frontend:** React + Vite · **Backend:** Python FastAPI · **Database:** SQLite

---

## Project Structure

```
quick-notes/
├── backend/
│   ├── main.py           # FastAPI app with SQLite
│   └── requirements.txt
├── frontend/
│   ├── index.html
│   ├── package.json
│   ├── vite.config.js
│   └── src/
│       ├── main.jsx
│       ├── App.jsx       # Main React component
│       └── index.css
└── README.md
```

---

## Getting Started

### 1 · Backend

```bash
cd backend

# Create & activate a virtual environment (recommended)
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Start the server
uvicorn main:app --reload --port 8000
```

The API will be available at `http://localhost:8000`.  
Interactive docs: `http://localhost:8000/docs`

### 2 · Frontend

```bash
cd frontend

npm install
npm run dev
```

Open `http://localhost:5173` in your browser.

---

## API Endpoints

| Method | Path             | Description         |
|--------|------------------|---------------------|
| GET    | `/notes`         | List all notes      |
| POST   | `/notes`         | Create a new note   |
| PUT    | `/notes/{id}`    | Update a note       |
| DELETE | `/notes/{id}`    | Delete a note       |
| GET    | `/health`        | Health check        |

---

## Features

- ✦ Create, read, update, and delete notes
- ✦ Notes stored in SQLite (auto-created on first run)
- ✦ Search/filter notes by title or content
- ✦ Amber pulse animation on fresh save
- ✦ Fully responsive layout

---

## Pushing to GitHub

```bash
# From the project root
git init
git add .
git commit -m "feat: initial QuickNotes full-stack app"

# Replace with your GitHub repo URL
git remote add origin https://github.com/YOUR_USERNAME/quick-notes.git
git branch -M main
git push -u origin main
```

---

## Tech Stack

| Layer     | Technology          |
|-----------|---------------------|
| Frontend  | React 18, Vite 5    |
| Styling   | Vanilla CSS         |
| Backend   | FastAPI, Uvicorn    |
| Database  | SQLite (via stdlib) |
| Fonts     | DM Sans, JetBrains Mono |
