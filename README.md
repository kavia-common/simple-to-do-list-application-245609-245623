# Simple To‑Do List Application (React)

## Overview

This repository contains a single-container React frontend application for a simple to-do list. The app is intended to support adding todos, marking them complete/incomplete, deleting them, and filtering the list (all/active/completed). Todos are persisted in the browser using localStorage, so no backend or database is required.

The frontend lives in `todo_app_frontend/` and runs on port 3000 in development.

## Features

The intended user-facing feature set for this project includes the ability to add new todos, toggle completion state, delete items, and filter by status (all, active, completed). The app is expected to persist the todo list to localStorage so that refreshing the page does not clear the list.

## Persistence (localStorage)

The application is designed to store todo state in the browser’s localStorage. This means:

- There is no server-side storage and no database.
- Data remains on the same browser/device until cleared (for example, by clearing site data).

## Project structure

- `todo_app_frontend/`: React application (Create React App / react-scripts)

## Running the frontend (local preview)

From the repository root:

```bash
cd todo_app_frontend
npm install
npm start
```

Then open:

- http://localhost:3000

## Environment variables

The frontend container includes a `.env` file under `todo_app_frontend/` with a set of `REACT_APP_*` variables. Create React App only exposes environment variables prefixed with `REACT_APP_` to the browser bundle.

These variables may be unused in a no-backend todo application, but they are defined in the current project:

- `REACT_APP_API_BASE`
- `REACT_APP_BACKEND_URL`
- `REACT_APP_FRONTEND_URL`
- `REACT_APP_WS_URL`
- `REACT_APP_NODE_ENV`
- `REACT_APP_NEXT_TELEMETRY_DISABLED`
- `REACT_APP_ENABLE_SOURCE_MAPS`
- `REACT_APP_PORT`
- `REACT_APP_TRUST_PROXY`
- `REACT_APP_LOG_LEVEL`
- `REACT_APP_HEALTHCHECK_PATH`
- `REACT_APP_FEATURE_FLAGS`
- `REACT_APP_EXPERIMENTS_ENABLED`

To change an environment variable, edit `todo_app_frontend/.env` and restart the dev server.

## Notes

This repository is frontend-only. If you are looking for backend endpoints or a database schema, they are intentionally not part of this project.
