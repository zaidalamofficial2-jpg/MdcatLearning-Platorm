# Alam Creative Academy — Learning Management System

A responsive, single-page LMS interface for **Alam Creative Academy**. The frontend is built with HTML, CSS and vanilla JavaScript. It includes student and administrator entry points and screens for learning resources, assessments and student progress.

## Features in the frontend

- Student login and student-account activation screens
- Separate administrator login screen
- Student dashboard and subject/chapter navigation
- Lecture and notes/resource views
- Test configuration, test runner and result views
- Doubt/support and progress views
- Student profile and administrator student-management screens
- Responsive layout with mobile navigation

> **Important — backend required:** This repository contains the frontend only. Authentication, sessions, student management, file uploads and persistent data are requested from a Node.js backend through `/api` endpoints. The original preview-only mock API and demo credentials have been removed. Without the matching backend, login and data-driven features will not work. GitHub Pages can host the static interface, but it cannot run the Node.js/SQLite backend.

## Run locally

You can open `index.html` directly to inspect the interface. For a local static server, from this folder run:

```bash
python -m http.server 8000
```

Then visit <http://localhost:8000>. This only serves the frontend; it does not provide the API backend.

## Deploy on GitHub Pages

1. Create a GitHub repository (for example, `alam-creative-academy-lms`).
2. Upload `index.html` and this `README.md` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`, then save.
6. Wait for GitHub Pages to publish the site.

The published page will show the frontend. To make login, student records and uploads functional, deploy the corresponding Node.js backend and SQLite/data storage separately, then configure the frontend API base URL to point to that backend. The backend source is not included in this frontend package, so its routes, security settings and hosting configuration must be supplied and verified separately.

## Project structure

```text
alam-creative-academy-lms/
├── index.html
└── README.md
```

## Technology

- HTML5
- CSS3
- Vanilla JavaScript
- Google Fonts (Poppins and Inter)
- Backend integration expected through HTTP `/api` routes

## Security note

Do not put real passwords, API secrets, private student information or database files in this public repository. Use HTTPS and secure server-side authentication/session handling in the backend.

## License

No license has been specified. All rights remain with the project owner unless a license is added to this repository.
