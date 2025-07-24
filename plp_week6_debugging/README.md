# 🐞 MERN Bug Tracker – Full Stack Debugging & Testing Showcase

An advanced bug tracking system built with the MERN stack (MongoDB, Express.js, React, Node.js), featuring a sleek, accessible frontend powered by **Tailwind CSS** and **shadcn/ui**. This project highlights deep integration of testing frameworks and debugging strategies across both client and server.

## 🚀 Key Features

- **Bug CRUD Operations** – Capture, modify, and remove bugs efficiently
- **Smart Filters** – Narrow results by status, severity, priority, or keyword
- **Live Dashboard** – Track bug counts and progress metrics
- **Collaborative Comments** – Leave notes and updates on bug threads
- **Lifecycle Tracking** – Visual status flow throughout resolution
- **Responsive UI** – Modern design built with Tailwind and shadcn/ui
- **Accessibility First** – WCAG compliance with ARIA support
- **Complete Test Suite** – Unit, integration, and e2e coverage
- **Robust Debugging** – Logs, error boundaries, and dev tooling

## 🧩 UI Tech Stack

This app uses:
- **Tailwind CSS** – Rapid utility-first styling
- **shadcn/ui** – Prebuilt accessible components
- **Lucide Icons** – Minimal icon system
- **Radix UI** – Headless design primitives

## 📦 Requirements

- Node.js v18+
- Local MongoDB or Atlas cluster
- npm or pnpm installed

## 🛠️ Setup

```bash
# Clone the repo
git clone <repository-url>
cd mern-bug-tracker

# Install dependencies
npm install
cd server && npm install
cd ../client && npm install

# Set environment variables
touch server/.env
```

Example `.env`:

```env
NODE_ENV=development
PORT=5000
MONGODB_URI=mongodb://localhost:27017/bug-tracker
```

```bash
# Start app
npm run dev
```

Runs frontend (port 3000) & backend (port 5000) concurrently.

## 🧪 Testing Strategy

### Backend

```bash
cd server
npm test           # Run all tests
npm run test:coverage
npm run test:watch
npm run test:debug
```

- Models, controllers, and middleware covered
- API endpoints verified via Supertest
- MongoDB Memory Server used for test isolation
- Coverage target: ≥ 70%

### Frontend

```bash
cd client
npm test
npm run test:coverage
npm run test:debug
```

- Component tests via Jest + React Testing Library
- API mocking using MSW
- Accessibility and behavior validated

## 🔍 Debugging Tools

- 🔧 Structured console logging with emoji-tagging
- 🕵️‍♂️ Node.js Inspector integration
- ⚠️ React error boundaries with fallback UI
- 🌐 DevTools: API tracing, component state, and console output

## 📁 Structure Snapshot

```
mern-bug-tracker/
├── client/
│   ├── src/components/ui/      # shadcn components
│   ├── src/components/         # Core UI: BugList, BugForm, etc.
│   ├── src/tests/              # Component/unit tests
│   ├── tailwind.config.js
├── server/
│   ├── models, controllers, routes, middleware
│   ├── tests/unit & integration
│   ├── setup.js                # test DB & mocks
├── package.json
├── README.md
```

## 🧪 Coverage Targets

| Scope         | Goal   |
|---------------|--------|
| Unit Tests    | ≥ 70%  |
| API Endpoints | Full   |
| UI Behaviors  | All critical paths |
| Accessibility | ARIA, contrast, keyboard nav |

## 🌐 API Highlights

- Full CRUD on `/api/bugs`
- Filtering: status, priority, severity, search
- Comments, status tracking, statistics endpoints

Example:
```http
GET /api/bugs?status=open&priority=high&search=login
```

## 🧠 Error Management

### Server

- Express error middleware
- Custom validation errors
- Graceful MongoDB disconnect
- Shutdown safety handlers

### Client

- Error boundaries
- Form-level validation
- API failure handling
- Dev-friendly fallbacks

## 🧰 Debugging Strategy

- Component-level logging
- API request interception and logging
- DevMode toggles for troubleshooting
- Real-time feedback on client/server interactions

## 🚀 Deployment Notes

- Set environment variables
- Use PM2 or similar for backend
- Build React for production
- Serve via CDN or container

## 🤝 Contribution Guide

- Fork → branch → code → test → PR
- Maintain 70%+ coverage
- Write tests for every feature added

## 📝 License

ISC License. Feel free to explore, fork, or extend the project.

## 🆘 Help & Support

- Review test samples and debugging workflows
- Refer to Tailwind and shadcn/ui docs
- Use browser and server logs to trace issues
