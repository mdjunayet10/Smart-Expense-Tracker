# Smart Expense Tracker

## Project Overview

Smart Expense Tracker is a frontend-only web application for recording, organizing, and reviewing personal expenses. It is built with HTML, CSS, and JavaScript and stores data in the browser using localStorage.

Course Name: Software Engineering Laboratory  
Course Code: CSE-3206  
Group No: 06  
Project Name: Smart Expense Tracker  

Group Members:

1. Al Sadique Nuhin - 23524202061
2. Md Junayet Hossain Mohit - 23524202065
3. Abdullah Mahmud Yamin - 23524202085
4. Mashrafi Elahi - 23524202137

## Current Features

- Frontend-only app with local browser storage persistence.
- Register, login, logout, and login persistence after page refresh.
- Demo forgot password flow that shows a local verification code on screen.
- Expense add, edit, delete, and receipt attachment support.
- Default expense categories: Food, Transport, Shopping, Bills, Entertainment, Health, Education, and Other.
- Overview dashboard with spending totals, recent expenses, category summary, and forecast information.
- Monthly budget tracking.
- Category budget tracking.
- Bill reminder calendar.
- Reports with spending distribution chart, report builder, and CSV export.
- Settings for profile, preferences, appearance, and backup/restore.
- JSON backup export and restore.
- Admin/demo account for user status management and system overview.
- Dark theme, theme color, and font size settings.
- English, Bangla, and Hindi language support for the main interface.
- Responsive layout for desktop and mobile browser use.

## How to Run

1. Open the project folder in VS Code or another editor.
2. Start a local static server, such as the VS Code Live Server extension.
3. Open `index.html` in a modern browser.

You can also use a simple local server:

```bash
python3 -m http.server 5500
```

Then open:

```text
http://localhost:5500
```

Do not run `assets/js/app.js` directly with Node. It is browser-side code and depends on `window`, `document`, and browser storage.

## Default Admin Account

- Email: `admin@expense.local`
- Password: `Admin1234`

The admin account can view the admin page, user account status controls, system summary, and audit activity.

## Project Structure

```text
Smart-Expense-Tracker/
├── assets/
│   ├── css/
│   │   └── style.css
│   └── js/
│       └── app.js
├── index.html
├── README.md
├── TESTING.md
├── .gitignore
├── Project_Methodology.pdf
├── SDLC.pdf
└── usecase_diagram.pdf
```

## Data Storage

This project stores app data in the user's browser storage. That includes local users, password hashes, expenses, budgets, receipts, settings, reminders, and audit history.

Important notes:

- There is no backend database.
- Data is not synced across devices.
- Clearing browser data can remove saved app data.
- Use the Export Full Backup option before clearing browser data or moving to another browser.
- Backup JSON files may contain local user data and password hashes, so they should not be shared publicly.

## Forgot Password Demo

The forgot password flow is a demo/local feature only. It does not send a real email.

The app checks the locally stored account email, generates a temporary verification code, and displays that code directly on the reset screen. The user can use the shown code to set a new password. The new password is stored using the same local password hashing method used by login/register.

## Backup And Restore

The Settings page includes:

- Export Full Backup
- Restore Backup JSON

Restore replaces the current local app data after confirmation. Invalid backup files are rejected before the app overwrites local data.

## Limitations

- No backend, server database, Firebase Auth, SMTP, or API is included.
- Authentication is local/demo authentication, not production-grade authentication.
- Forgot password is demo/local only and does not send real OTP or email.
- Browser storage can be cleared by the user or browser.
- Large receipt files may increase browser storage usage.
- This project is intended for academic frontend demonstration, not production financial storage.

## Future Improvements

- Backend database and secure server-side authentication.
- Real email verification and password recovery.
- Cloud sync across devices.
- Stronger role and access control.
- Automated tests.
- Production deployment with secure hosting.

## Final Package Guidance

For final submission, include:

- `index.html`
- `assets/`
- `README.md`
- `TESTING.md`
- `.gitignore`
- Project PDFs/docs

Exclude:

- `.git/`
- `.venv/`
- `.DS_Store`
- `__MACOSX/`
- temporary/cache files
- editor/system junk files
