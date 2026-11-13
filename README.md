# Richfield Connect

**Module:** Web Technology 512
**Assignment Title:** Richfield Connect Platform SPA
**Student Name:** [Insert your full name and surname]
**Student Number:** [Insert your student number]

## Project Description
Richfield Connect is an academic social engagement Single-Page Application (SPA) built with React 18, React Router v6 and the Context API (`useReducer`), with state persisted in `localStorage`.

Students create a profile (with real-time validation and a live preview), then use the feed to post updates, like posts and delete their own posts.

## Component Architecture
* `App` – root; wraps the app in the Context provider and defines routes (`/` feed, `/signup` sign-up; the feed redirects to `/signup` when no profile exists).
* `AppContext` – global state (`user`, `posts`) via `useReducer`, synced to `localStorage`. Actions: `SIGN_UP`, `SIGN_OUT`, `ADD_POST`, `TOGGLE_LIKE`, `DELETE_POST`.
* `Navbar` & `Footer` – persistent navigation UI.
* `SignUp` & `ProfilePreview` – controlled form with real-time validation and live preview.
* `Feed`, `CreatePost`, `Post` – post creation, liking and deletion (only the author can delete a post).

## How to Run the Application Locally
1. Extract the project folder.
2. Run `npm install`.
3. Run `npm run dev` and open the printed local address (e.g. `http://localhost:5173`).

To produce a production build, run `npm run build`.

## Notes
* Data is stored in the browser's `localStorage` only; there is no backend. Passwords are validated but never stored.

## External Resources and Tutorials Referenced
* React Documentation: https://react.dev/learn
* React Router v6 Documentation: https://reactrouter.com/en/main
* MDN Web Docs - localStorage: https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage
