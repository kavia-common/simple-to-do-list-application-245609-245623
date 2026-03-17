# React To‑Do App (Frontend)

## Overview

This folder contains the React frontend for a simple to-do list application. The app is intended to provide a clean, simple UI for managing todos entirely in the browser, without any backend service.

The application is run using Create React App (`react-scripts`).

## Features

This project’s intended functionality includes:

- Adding new todos.
- Marking todos as complete or incomplete.
- Deleting todos.
- Filtering the list by status (all, active, completed).
- Persisting todos in the browser using localStorage so that reloads keep your list.

## Persistence (localStorage)

Todo data is designed to be saved in the browser’s localStorage. This means:

- No backend or database is required.
- Todos are stored per browser profile and per origin (URL).
- Clearing browser storage/site data will remove saved todos.

## Getting started

### Install dependencies

From this folder:

```bash
npm install
```

### Run the frontend preview (development)

```bash
npm start
```

Then open:

- http://localhost:3000

If port 3000 is unavailable, Create React App may prompt to use another port when run interactively. In CI or non-interactive contexts, configure the port via environment variables or ensure 3000 is free.

### Run tests

```bash
npm test
```

### Build for production

```bash
npm run build
```

The production build output is generated in `build/`.

## Environment variables

This project includes a `.env` file in this directory. In Create React App, only variables prefixed with `REACT_APP_` are embedded into the frontend bundle.

The currently defined variables are:

- `REACT_APP_API_BASE`: Base URL for API calls (may be unused for a localStorage-only app).
- `REACT_APP_BACKEND_URL`: Backend URL (may be unused).
- `REACT_APP_FRONTEND_URL`: The frontend URL.
- `REACT_APP_WS_URL`: WebSocket URL (may be unused).
- `REACT_APP_NODE_ENV`: Environment name (for example, `development`).
- `REACT_APP_NEXT_TELEMETRY_DISABLED`: Telemetry control flag.
- `REACT_APP_ENABLE_SOURCE_MAPS`: Whether source maps are enabled.
- `REACT_APP_PORT`: Preferred dev server port (commonly 3000).
- `REACT_APP_TRUST_PROXY`: Proxy trust flag (usually unused in CRA).
- `REACT_APP_LOG_LEVEL`: Log level (app-dependent).
- `REACT_APP_HEALTHCHECK_PATH`: Healthcheck path (app-dependent).
- `REACT_APP_FEATURE_FLAGS`: Feature flag configuration (app-dependent).
- `REACT_APP_EXPERIMENTS_ENABLED`: Experiment toggle.

After changing `.env`, restart the dev server so changes take effect.

## Technology

- React
- Create React App (`react-scripts`)
- Vanilla CSS for styling

## Repository note

This is a frontend-only project. There is no backend container and no database by design.
