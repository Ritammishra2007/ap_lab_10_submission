# AP_Project — MiniTube

A YouTube-like video streaming platform built with Node.js/Express and React, using file-based storage for videos and metadata.

## 📁 Project Structure

```
ap_project/
├── backend/              # Express.js API server
│   ├── server.js
│   ├── package.json
│   ├── routes/           # API route handlers
│   ├── data/             # JSON data files (videos, watch history)
│   └── media/            # Video files
├── frontend/             # React.js client
│   ├── package.json
│   ├── public/
│   ├── src/
│   │   ├── App.js
│   │   ├── components/
│   │   └── ...
│   └── ...
└── README.md
```

## 🚀 Getting Started

### Prerequisites
- Node.js and npm installed

### Backend Setup

1. Navigate to the backend directory:
```bash
cd backend
```

2. Install dependencies:
```bash
npm install
```

3. Start the server:
```bash
npm run dev
```

The server will be available at `http://localhost:4000`

### Frontend Setup

1. In a new terminal, navigate to the frontend directory:
```bash
cd frontend
```

2. Install dependencies:
```bash
npm install
```

3. Start the React development server:
```bash
npm start
```

The frontend will automatically open at `http://localhost:3000`

## ✨ Features

- **Video Search**: Search videos by title in real-time
- **Video Player**: Watch videos with HTML5 player controls
- **Like System**: Like/unlike videos
- **Comments**: Add and view comments on videos
- **Watch History**: Track watched videos with timestamps
- **Clear History**: Delete watch history
- **Responsive Design**: Works on desktop and mobile devices
- **Modern UI**: Sci-fi themed with smooth animations

## 📡 API Endpoints

### Videos
- `GET /api/videos` — List all videos
- `GET /api/videos?title=query` — Search videos by title
- `GET /api/videos/:id` — Get single video (increments views)
- `PUT /api/videos/:id/like` — Like a video
- `PUT /api/videos/:id/comments` — Add comment
- `GET /api/videos/:id/comments` — Get comments

### Watch History
- `GET /api/videos/watch-history` — Get watch history
- `POST /api/videos/watch-history` — Add to history
- `DELETE /api/videos/watch-history` — Clear history

## � Notes

- **Backend**: Uses file-based storage (JSON files) for videos and watch history
- **Port**: Backend runs on `http://localhost:4000`
- **API**: Frontend communicates with backend via `/api` endpoints

## 📦 Dependencies

### Backend
- express
- cors
- body-parser
- nodemon (dev)

### Frontend
- react
- react-dom
- axios
- react-scripts

## 🎨 UI Components

- **Header**: Search bar and branding
- **VideoPlayer**: Full-screen video with controls
- **CommentSection**: View and add comments
- **Sidebar**: Video thumbnails and watch history tabs
- **Responsive Layout**: Adapts to mobile and tablet screens

## 🔧 Development

To develop locally:

1. Keep backend running: `npm run dev` in `/backend`
2. Keep frontend running: `npm start` in `/frontend`
3. Update React components in `/frontend/src/`
4. Backend hot-reloads on file changes (nodemon)

## 📝 License

MIT
