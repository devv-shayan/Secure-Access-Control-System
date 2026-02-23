# Secure Access Control System Demo

## Demo Folder Tree

Use this exact structure at the project root for the demo:

```text
Secure-Access-Control-System/
├── app.py
├── requirements.txt
├── app.db                  # SQLite database file (created automatically at runtime)
└── templates/
    ├── login.html
    ├── register.html
    └── dashboard.html
```

## Run Commands (Copy/Paste)

```bash
python -m venv .venv
# Activate virtual environment:
# macOS/Linux:
source .venv/bin/activate
# Windows (PowerShell):
.venv\\Scripts\\Activate.ps1
pip install -r requirements.txt
python app.py
```

## Quick Human Demo Script

1. Open the app in your browser (for example `http://127.0.0.1:5000`).
2. Go to the **Register** page and create a new user (username + password).
3. Go to **Log In** and sign in with the same credentials.
4. Confirm you can see the protected **Dashboard** page after login.
5. Click **Log Out**.
6. Manually enter the dashboard URL (for example `/dashboard`) after logout.
7. Verify access is blocked (redirect to login or unauthorized response), proving route protection is active.

## Troubleshooting

- **Duplicate username error**: If registration fails because the username already exists, choose a different username or delete the existing row from the SQLite database.
- **Virtual environment not activated**: If `pip install` targets the wrong Python or imports fail, activate `.venv` first, then rerun install/start commands.
- **Port conflict**: If port `5000` is already in use, run with another port (e.g., `flask run --port 5001`) or change the app's configured `port` in `app.py`.
