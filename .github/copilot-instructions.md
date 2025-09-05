# Copilot Instructions for RepoPython

## Overview
This project is a simple Flask-based login system. It uses in-memory user authentication (no database), modern UI, and session management. The codebase is minimal and designed for clarity and quick iteration.

## Architecture & Key Files
- `app.py`: Main Flask app. Defines all routes, user logic, and session handling. Users are hardcoded in the `USERS` dictionary.
- `templates/`: Contains Jinja2 HTML templates (`login.html`, `welcome.html`).
- `static/style.css`: Custom CSS for modern look and dark mode.
- `requirements.txt`: Only dependency is `Flask`.

## Developer Workflows
- **Run locally:**
  1. Install dependencies: `pip install -r requirements.txt`
  2. Start app: `python app.py`
  3. Visit [http://localhost:5000](http://localhost:5000)
- **No database or migrations**: All user data is in-memory in `app.py`.
- **Debug mode**: Enabled by default (`debug=True` in `app.run`).
- **No tests or CI/CD**: Add your own if needed.

## Project-Specific Patterns
- **User Auth**: Only three users, defined in `USERS` dict. No registration or password reset.
- **Session**: Flask session stores `username` and `email` after login.
- **Flash messages**: Used for login success/error and logout notifications.
- **Cache busting**: Static files use a query param with file mtime for cache busting (see `dated_url_for`).
- **UI**: Modern, responsive, with dark mode toggle in `login.html` and `style.css`.

## Conventions
- Spanish language for UI and code comments.
- Minimal external dependencies (only Flask, FontAwesome, Google Fonts via CDN).
- All logic in a single file (`app.py`) for simplicity.
- No environment variable management; secret key is hardcoded for demo purposes.

## Examples
- To add a new user, edit the `USERS` dict in `app.py`.
- To change the look, edit `static/style.css` and templates.
- To add new routes, define them in `app.py` and create corresponding templates.

## References
- See `README.md` for user credentials and quickstart.
- See `GITHUB_GUIDE.md` for Git/GitHub workflow tips.

---
If you add new features, document any new conventions or workflows here.
