# Expense Tracker — Project Memory

## Tech Stack & Commands
- **Framework:** Vite + React (Frontend Starter)
- **Styling:** Tailwind CSS
- **Build Command:** `npm run build`
- **Dev Server Command:** `npm run dev`
- **Linting:** `npm run lint` (using eslint.config.js)

## Project Structure
- `src/` - Application source code
- `src/components/` - UI components (Transaction lists, forms)
- `public/` - Static assets
- `index.html` - Main application entry page

## Coding Guidelines
- **State Management:** Prefer React hooks (`useState`, `useEffect`) for managing transaction states component-side.
- **Components:** Use functional components with descriptive semantic HTML names.
- **Code Style:** Follow strict clean code patterns—keep functions short, modular, and single-purpose.
- **Naming Conventions:** Use `camelCase` for variables and functions (e.g., `handleDeleteTransaction`), and `PascalCase` for component files.

## Architectural Rules
- **Modular Architecture:** `App.jsx` acts as the primary state container. Features (like `Summary`, `AddTransaction`, and `TransactionList`) must be extracted into isolated components in `src/components/`.
- **State Colocation:** Keep local UI state (e.g., form inputs, filter selections) contained within the specific child components that use them, separating them from the main global `transactions` state.
- **Data Type Integrity:** Always ensure numeric data (like transaction `amount`) is stored and processed strictly as `Number` types to prevent string concatenation bugs.
- Never hardcode dynamic sample data once live state features are added.
- Always check component prop types or destructuring rules when passing transaction arrays down the tree.