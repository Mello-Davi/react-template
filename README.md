# React Project Template

This repository is a blank-slate template configured for developing scalable and modern web applications. It integrates essential tools for routing, styling, state management, and validation.

## Architecture and Technologies

This project is built using:
- React 19
- React Router v8
- Vite
- TypeScript
- Tailwind CSS v4
- Zustand (Global State Management)
- React Hook Form + Zod (Form Validation)
- Axios (HTTP Client)
- JSON Server (Mock Backend)
- ESLint (Code Quality)

## Project Structure

The codebase is organized inside the `app/` directory to maintain separation of concerns:

- `app/routes/`
  Contains the application route definitions and components that map directly to URLs. Logic for data fetching (loaders) and mutations (actions) specific to a route should reside here.

- `app/pages/`
  Contains full-page UI compositions. Use this to construct complex views while keeping the files inside `app/routes/` focused solely on routing and data aggregation.

- `app/components/`
  Contains reusable, generic, and modular UI components (e.g., buttons, inputs, modals) that can be shared across different pages and routes.

- `app/hooks/`
  Contains custom React hooks for shared logic, abstracting side effects or complex behaviors outside of components.

- `app/stores/`
  Contains Zustand store configurations. Global states should be split logically into modular files within this directory.

- `app/assets/`
  Contains static assets such as images, icons, and local fonts.

## Running the Project

Ensure you have Node.js and `pnpm` installed.

1. **Install dependencies:**
   ```bash
   pnpm install
   ```

2. **Start the development server:**
   ```bash
   pnpm run dev
   ```

3. **Build the project for production:**
   ```bash
   pnpm run build
   ```

4. **Preview the production build:**
   ```bash
   pnpm run start
   ```

5. **Type checking and Linting:**
   To verify TypeScript errors and run linting rules:
   ```bash
   pnpm run typecheck
   # For linting (if configured in package.json):
   pnpm run lint
   ```

## Development Guidelines

- **Forms:** Build forms using `react-hook-form` and perform data validation using `zod`.
- **State Management:** Keep React components mostly stateless and manage global states inside `app/stores/` with `zustand`.
- **Styling:** Utilize Tailwind CSS utility classes instead of creating custom CSS files whenever possible.
- **Requests:** Use `axios` for standard HTTP requests. During development, mock REST endpoints using `json-server`.
