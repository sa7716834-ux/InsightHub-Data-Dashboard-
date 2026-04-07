# 📊 InsightHub — Intelligent Data Dashboard

A clean, production-ready web platform to upload, visualize, analyze, and export data from Excel and CSV files — powered by AI insights.

## ✨ Features

- **File Upload** — Drag & drop CSV or Excel (.xlsx/.xls) files up to 100MB
- **Interactive Charts** — Bar, line, pie, donut, scatter — live chart switching
- **Smart Data Table** — Search, filter, sort, paginate across all columns
- **AI Insights** — Ask plain-English questions about your dataset (Claude AI)
- **Export Reports** — PDF, CSV, Excel, and JSON export with one click
- **Summary Statistics** — Min, max, mean, median, std dev per column
- **Data Profiling** — Column type, null count, unique value detection
- **User Auth** — Login, register, role-based access (Admin / Analyst / Viewer)
- **Demo Datasets** — Sales, Financial, and Academic data built-in

## 🖥️ Pages

| Page | File | Description |
|------|------|-------------|
| Landing | `index.html` | Marketing page with feature overview |
| Login/Register | `login.html` | Auth with demo credentials |
| Dashboard | `dashboard.html` | Full app — charts, table, AI, exports |

## 🚀 Quick Start

### Option 1: Open locally (zero setup)
```bash
git clone https://github.com/YOUR_USERNAME/InsightHub.git
cd datalens
# Open index.html in your browser — that's it!
open index.html
```

### Option 2: GitHub Pages (free hosting)
1. Push to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)`
4. Your site is live at `https://YOUR_USERNAME.github.io/InsightHub`

### Option 3: Any static host
Drop the 3 HTML files on Netlify, Vercel, or any web server — no build step needed.

## 🔑 Demo Credentials

| Role | Email | Password |
|------|-------|----------|
| Admin | `admin@datalens.demo` | `admin123` |
| Analyst | `analyst@datalens.demo` | `analyst123` |

> **Note:** Auth is localStorage-based for demo mode. For production, replace with a real backend.

## 🤖 AI Integration

DataLens uses the **Claude API** (claude-sonnet-4-20250514) for AI data insights.

- In demo mode, AI uses smart local fallback responses
- For live AI: the fetch call in `dashboard.html` targets `https://api.anthropic.com/v1/messages`
- The API key is handled server-side — never hardcode it in client JS
- For production deployment, proxy the API call through your backend

## 📁 Project Structure

```
datalens/
├── index.html        # Landing page
├── login.html        # Authentication
├── dashboard.html    # Main dashboard app
├── README.md         # This file
└── .gitignore        # Protects sensitive files
```

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| HTML5 / CSS3 / Vanilla JS | Core — zero build tools |
| Chart.js 4.4 | Interactive charts |
| SheetJS (xlsx) | Excel/CSV parsing |
| jsPDF + AutoTable | PDF export |
| Google Fonts (DM Sans + DM Mono) | Typography |
| Claude API | AI data insights |
| localStorage | Session & user storage (demo) |

## 🎨 Design System

- **Background:** `#F8FAFC` (cool white)
- **Primary:** `#2563EB` (blue)
- **Success:** `#10B981` (green)
- **Warning:** `#F59E0B` (amber)
- **Error:** `#EF4444` (red)
- **Font:** DM Sans (UI) + DM Mono (data/numbers)

## 🔒 Security Notes

- All API keys belong in `.env` / server environment — never in client JS
- The `.gitignore` excludes `.env` and any config files with secrets
- User passwords in demo mode are stored in `localStorage` (plain text — for demo only)
- For production: use a backend with bcrypt hashing and JWT sessions

## 📦 Production Upgrade Path

To upgrade from demo to production:

1. **Backend:** Add FastAPI or Node.js backend for auth + data storage
2. **Database:** PostgreSQL or SQLite for user/dataset persistence
3. **AI proxy:** Route Claude API calls through your backend (never expose keys client-side)
4. **Auth:** Replace localStorage with JWT + bcrypt
5. **Storage:** Use S3 or similar for uploaded file storage

## 📄 License

MIT — free to use, modify, and distribute.

---

Built by **Syed Saif Ali**
