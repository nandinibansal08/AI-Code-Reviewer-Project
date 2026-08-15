# 🤖 AI Code Reviewer — Frontend

AI Code Reviewer is a modern web application that allows developers to submit their code and receive AI-powered code reviews. The frontend provides an interactive code editor, authentication screens, review history, syntax highlighting, and an interface for managing previous code reviews.

This repository contains the **frontend application**, built with React and Vite.

---

## 📌 What This Project Does

The AI Code Reviewer frontend provides an interactive platform where users can:

* Write or paste code into an online code editor.
* Submit code for an AI-powered review.
* View AI-generated feedback.
* View previous code reviews.
* Select previous reviews and view their code and feedback.
* Edit existing reviews.
* Delete previous reviews.
* Register and log in to their account.
* Communicate with the backend API using Axios.

The frontend communicates with the backend through REST APIs for authentication and AI code-review functionality.

### Application Flow

```text
User
  ↓
Register / Login
  ↓
Authentication Token
  ↓
Code Editor
  ↓
Submit Code
  ↓
Backend API
  ↓
AI Code Review
  ↓
Display Review
  ↓
Save Review History
  ↓
View / Edit / Delete Previous Reviews
```

---

# 🛠️ Technologies Used

## Frontend

* **React 19** — Building the user interface
* **Vite** — Development server and build tool
* **JavaScript (ES6+)** — Application logic
* **Tailwind CSS** — Styling and responsive UI
* **React Router DOM** — Client-side routing
* **Axios** — Communication with backend REST APIs

## Code Editor & Syntax Highlighting

* **react-simple-code-editor** — Interactive code editor
* **PrismJS** — Code syntax highlighting
* **Highlight.js** — Syntax highlighting for rendered content
* **React Markdown** — Rendering AI-generated Markdown responses
* **rehype-highlight** — Syntax highlighting for Markdown code blocks

## UI

* **React Icons** — Edit, delete, and other interface icons

## Backend Communication

The frontend communicates with the backend using REST APIs through Axios.

Example endpoints used by the frontend:

```text
POST   /auth/register
POST   /auth/login

POST   /ai/get-review
GET    /ai/past-prompts
PUT    /ai/past-prompts/:id
DELETE /ai/past-prompts/:id
```

---

# ✨ Features

### 🔐 User Authentication

Users can:

* Create an account.
* Log in using their email and password.
* Receive an authentication token.
* Use the token to access protected AI review APIs.

---

### 💻 Interactive Code Editor

Users can write or paste their code directly into the application.

The editor provides:

* Code editing
* Syntax highlighting
* Developer-friendly interface
* Preloaded sample code

Example:

```javascript
function sum() {
  return 1 + 1;
}
```

---

### 🤖 AI Code Review

Users can submit their code for review.

The frontend sends the code to the backend:

```text
POST /ai/get-review
```

The AI-generated feedback is then displayed to the user.

---

### 📜 Previous Reviews

Users can access their previous code reviews from the sidebar.

Each previous review contains:

* Submitted code
* AI-generated review
* Review ID

Users can select a previous review to view it again.

---

### ✏️ Edit Reviews

Users can select a previous review and modify the code/review.

The frontend communicates with:

```text
PUT /ai/past-prompts/:id
```

---

### 🗑️ Delete Reviews

Users can remove previous reviews from their history.

The frontend sends:

```text
DELETE /ai/past-prompts/:id
```

---

### 📝 Markdown Support

AI-generated responses can contain Markdown formatting.

The project uses:

* `react-markdown`
* `rehype-highlight`

to render formatted AI responses and code blocks.

---

### 🎨 Responsive UI

The interface uses Tailwind CSS and responsive layouts to provide a clean developer-oriented experience across different screen sizes.

---

# 📂 Project Structure

```text
frontend/
│
├── public/
│
├── src/
│   ├── assets/
│   │
│   ├── components/
│   │   ├── Login.jsx
│   │   └── Register.jsx
│   │
│   ├── App.jsx
│   ├── App.css
│   ├── index.css
│   └── main.jsx
│
├── eslint.config.js
├── index.html
├── package.json
├── package-lock.json
├── vite.config.js
└── README.md
```

---

# ⚙️ How to Run It Locally

## 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Example:

```bash
git clone https://github.com/YOUR_USERNAME/ai-code-reviewer-frontend.git
```

---

## 2. Navigate to the Frontend Folder

```bash
cd ai-code-reviewer-frontend
```

If your repository contains both backend and frontend:

```bash
cd frontend
```

---

## 3. Install Dependencies

Run:

```bash
npm install
```

This installs all dependencies listed in `package.json`.

---

## 4. Start the Development Server

Run:

```bash
npm run dev
```

Vite will start the development server.

You should see something similar to:

```text
Local: http://localhost:5173/
```

Open this URL in your browser.

---

# 🔗 Backend Requirement

This frontend communicates with a backend running on:

```text
http://localhost:3000
```

The current frontend uses API requests such as:

```javascript
axios.post("http://localhost:3000/ai/get-review", ...)
```

Therefore, the backend must be running for authentication and AI code-review functionality to work.

### Backend APIs Used

| Method | Endpoint               | Purpose                   |
| ------ | ---------------------- | ------------------------- |
| POST   | `/auth/register`       | Register a new user       |
| POST   | `/auth/login`          | Authenticate user         |
| POST   | `/ai/get-review`       | Submit code for AI review |
| GET    | `/ai/past-prompts`     | Get previous reviews      |
| PUT    | `/ai/past-prompts/:id` | Update a review           |
| DELETE | `/ai/past-prompts/:id` | Delete a review           |

---

# 📸 Screenshots

Add screenshots of your application inside a `screenshots` folder.

Recommended structure:

```text
frontend/
│
├── screenshots/
│   ├── login.png
│   ├── register.png
│   ├── code-editor.png
│   ├── ai-review.png
│   └── previous-reviews.png
│
└── README.md
```

Then add them to this README.

## 🔐 Login

![Login Page](screenshots/login.png)

---

## 📝 Registration

![Registration Page](screenshots/register.png)

---

## 💻 Code Editor

![Code Editor](screenshots/code-editor.png)

---

## 🤖 AI Code Review

![AI Code Review](screenshots/ai-review.png)

---

## 📜 Previous Reviews

![Previous Reviews](screenshots/previous-reviews.png)

> Replace the screenshot filenames above with the actual screenshots you add to your repository.

---

# 🌐 Live Demo

**Live Application:**
YOUR_LIVE_DEMO_URL

Example:

```text
https://your-project.vercel.app
```

> Replace `YOUR_LIVE_DEMO_URL` with your actual deployed frontend URL.

---

# 💻 GitHub Repository

**Source Code:**
YOUR_GITHUB_REPOSITORY_URL

Example:

```text
https://github.com/YOUR_USERNAME/ai-code-reviewer-frontend
```

---

# 🧑‍💻 Development Commands

### Install dependencies

```bash
npm install
```

### Run development server

```bash
npm run dev
```

### Build for production

```bash
npm run build
```

### Preview production build

```bash
npm run preview
```

### Run ESLint

```bash
npm run lint
```

---

# 🚀 Production Build

To create an optimized production build:

```bash
npm run build
```

The production files will be generated in:

```text
dist/
```

You can then deploy the generated application using a suitable frontend hosting platform.

---

# 🔮 Future Improvements

Potential improvements for future versions include:

* 🌐 Use environment variables for backend API URLs.
* 🔄 Add loading indicators while AI reviews are being generated.
* ❌ Display user-friendly error messages.
* 🎨 Improve authentication UI.
* 📱 Further optimize mobile responsiveness.
* 🌙 Add theme switching.
* 📊 Add detailed code-review analytics.
* 🔍 Add programming-language selection.
* 💾 Add export/download of AI reviews.
* 🔗 Add direct links between frontend and deployed backend.
* 🧪 Add automated frontend testing.

---

# 📄 License

This project is developed for educational and portfolio purposes.

---

# 👩‍💻 Author

**Nandini Bansal**

B.Tech – Computer Science Engineering

Interested in **Full Stack Development, React, AI-powered applications, and modern web technologies**.

---

⭐ If you find this project useful, consider giving the repository a star!
