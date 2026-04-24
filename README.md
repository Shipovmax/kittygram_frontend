# Kittygram Frontend

React frontend for the [Kittygram](https://github.com/Shipovmax/kittygram_final) cat photo sharing platform.

---

## Features

- **Auth** — sign up, sign in, token-based session via `localStorage`
- **Cat feed** — paginated list of cat cards on the main page
- **Cat card** — view individual cat with photo, name, year of birth, and achievements
- **Add / Edit / Delete** — full CRUD for cat cards (authenticated users only)
- **Protected routes** — unauthenticated users are redirected to `/signin`
- **Context API** — global user state via `UserContext`
- **CSS Modules** — scoped styles per component

---

## Tech Stack

| | |
|---|---|
| Language | JavaScript |
| Framework | React 17 |
| Routing | React Router DOM v5 |
| Styles | CSS Modules |
| API | REST (Django backend) |

---

## Quick Start

```bash
git clone https://github.com/Shipovmax/kittygram_frontend
cd kittygram_frontend

npm install
npm start
```

UI at `http://localhost:3000`

Backend must be running at `http://localhost:8000` (see [kittygram_final](https://github.com/Shipovmax/kittygram_final)).

---

## Routes

| Path | Component | Auth required |
|------|-----------|---------------|
| `/` | MainPage — cat feed with pagination | Yes |
| `/signin` | SignIn | No |
| `/signup` | SignUp | No |
| `/cats/add` | AddCardPage | Yes |
| `/cats/edit` | EditCardPage | Yes |
| `/cats/:id` | CardPage | Yes |

---

## Project Structure

```
src/
├── components/
│   ├── app/              # Root component, routing, UserContext provider
│   ├── header/           # Navigation + logout
│   ├── footer/
│   ├── main-page/        # Paginated cat feed
│   ├── card-page/        # Single cat view
│   ├── add-card-page/    # Create cat form
│   ├── edit-card-page/   # Edit cat form
│   ├── sign-in/
│   ├── sign-up/
│   ├── main-card/        # Cat card component
│   ├── pagination-box/
│   ├── popup/
│   └── ui/               # Reusable: Button, Checkbox, Select, Modal, ProtectedRoute
└── utils/
    ├── api.js            # All API calls (fetch wrapper)
    ├── constants.js      # Base URL, token key
    └── context.js        # UserContext definition
```

---

## Author

- GitHub: [Shipovmax](https://github.com/Shipovmax)
- Email: shipov.max@icloud.com
