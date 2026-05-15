# ✦ Taskflow — AI-Powered Task Manager

A full-stack task management web application built with vanilla HTML, CSS, and JavaScript, featuring user authentication, CRUD operations, real-time UI updates, and an integrated Claude AI assistant.
 
---

## 🚀 Features

- **User Authentication** — Sign up, sign in, and sign out with session-based user isolation
- **Task CRUD** — Create, read, update, and delete tasks with full metadata
- **Priority & Labels** — Organize tasks by priority (High / Medium / Low) and labels (Work, Personal, Urgent, Design)
- **Smart Views** — Filter tasks by Today, Upcoming, Completed, or by label
- **Live Search** — Instant full-text search across task titles and descriptions
- **Stats Dashboard** — Real-time counts for total, active, completed, and overdue tasks
- **AI Assistant** — Claude-powered sidebar assistant with context-aware task advice
- **Responsive Design** — Works across desktop and mobile screen sizes

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| AI Integration | Anthropic Claude API (`claude-sonnet-4-20250514`) |
| Styling | CSS custom properties, Flexbox, CSS Grid |
| Icons | Tabler Icons |
| Hosting | Static file (no backend required) |

---

## 📁 Project Structure

```
taskflow/
├── index.html       # Main application (single-file)
└── README.md        # Project documentation
```

> The entire application lives in a single `index.html` file — no build tools, no frameworks, no dependencies to install.

---

## ⚡ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/taskflow.git
cd taskflow
```

### 2. Add your Anthropic API key

Open `index.html` and find the `fetch` call to the Anthropic API. Add your key to the request headers:

```javascript
headers: {
  'Content-Type': 'application/json',
  'x-api-key': 'YOUR_ANTHROPIC_API_KEY',   // add this line
  'anthropic-version': '2023-06-01'
}
```

> Get your API key at [console.anthropic.com](https://console.anthropic.com)

### 3. Open in browser

```bash
# Option A — open directly
open index.html

# Option B — serve locally (recommended)
npx serve .
# or
python -m http.server 8080
```

Then visit `http://localhost:8080`

---

## 🔐 Demo Account

| Field | Value |
|---|---|
| Email | `demo@taskflow.app` |
| Password | `demo1234` |

Or create a new account from the sign-up tab.

---

## 🤖 AI Assistant

The built-in AI assistant (powered by Claude) reads your live task data and can:

- Summarize your current workload
- Suggest what to focus on today
- Flag overdue or high-priority tasks
- Answer any productivity question in natural language

Type a question in the right-hand panel or use the quick-action chips.

---

## 📌 Key Concepts Demonstrated

- **Full-stack app structure** — auth flow, state management, data persistence (in-memory)
- **API integration** — calling the Anthropic REST API with `fetch`, handling streaming-style responses
- **Dynamic data handling** — reactive UI updates without a framework, live filtering and search
- **Component-style architecture** — modular render functions and event-driven state

---

## 🗺 Roadmap / Possible Improvements

- [ ] Backend persistence (Node.js + SQLite or Supabase)
- [ ] Real-time sync with WebSockets
- [ ] Drag-and-drop task reordering (Kanban board view)
- [ ] Due date reminders / notifications
- [ ] Dark/light mode toggle
- [ ] Export tasks to CSV or PDF
- [ ] OAuth (Google / GitHub sign-in)

---

## 📄 License

MIT — free to use, modify, and distribute.

---

> Built with ✦ and Claude by Anthropic
