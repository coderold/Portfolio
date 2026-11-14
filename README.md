# Portfolio

A personal portfolio built with React and Vite. The project is currently a small starter: `src/App.jsx` renders a heading and a Lucide camera icon, with the rest of the portfolio still to build.

## Tech stack

- **React 19** (`react`, `react-dom`) for the UI, written in JavaScript and JSX.
- **Vite 8** for the development server and production builds.
- **Tailwind CSS 4** for utility-first styling, connected to Vite through `@tailwindcss/vite`.
- **Radix Themes** (`@radix-ui/themes`) is installed for accessible, pre-styled UI components. It is not currently used in the app.
- **Lucide React** (`lucide-react`) for icons. `Camera` is currently used in `src/App.jsx`.

### Development tools and plugins

- **`@vitejs/plugin-react`** enables React support in Vite.
- **ESLint 10** checks the code, with `@eslint/js` and `globals`.
- **`eslint-plugin-react-hooks`** checks React Hooks usage.
- **`eslint-plugin-react-refresh`** provides Vite/React Fast Refresh lint rules.
- **`@types/react`** and **`@types/react-dom`** are installed, though the app currently uses JavaScript rather than TypeScript.

## Getting started

### Requirements

- Node.js **20.19 or newer** (or 22.12 or newer), as required by Vite 8 and its plugins.
- npm.

### Install and run

```sh
npm install
npm run dev
```

Open the local URL printed by Vite in your terminal. If the `vite: not found` message appears, install the project dependencies with `npm install` from the project directory.

## Useful commands

| Command | Purpose |
| --- | --- |
| `npm run dev` | Start the local development server with hot reload. |
| `npm run build` | Create the production build in `dist/`. |
| `npm run preview` | Preview the production build locally; run `npm run build` first. |
| `npm run lint` | Run ESLint across the project. |

## Project layout

```text
index.html          HTML entry point and page metadata
public/             Static files served as-is (for example, favicon.svg)
src/
  main.jsx          React entry point; mounts App
  App.jsx           Main page component
  index.css         Tailwind import and global/theme styles
  App.css           Additional component styles (not currently imported)
  assets/           Images and other files imported by source code
vite.config.js      Vite, React, and Tailwind plugin configuration
eslint.config.js    ESLint configuration
```

## Continuing the portfolio

1. **Build the page in `src/App.jsx`.** Replace the starter heading and icon with the portfolio sections you need, such as an introduction, projects, skills, experience, and contact links.
2. **Add components as the page grows.** Keep reusable sections in `src/` (for example, `src/components/ProjectCard.jsx`) and import them into `App.jsx`.
3. **Style consistently.** Tailwind is available in JSX, and the shared theme tokens and global styles live in `src/index.css`. `src/App.css` is available for regular CSS, but import it from the component that needs it before relying on its styles.
4. **Add images and icons.** Put imported images in `src/assets/`; put files that should be served directly at a stable URL in `public/`. Use icons from `lucide-react` where appropriate.
5. **Use Radix Themes if wanted.** It is a dependency but is not wired into the current app yet. Follow its setup instructions before using its themed components so the theme provider and styles are configured.
6. **Check the result.** Run `npm run lint` and `npm run build` before publishing. Deploy the generated `dist/` directory using a static hosting provider that supports single-page applications.

The dependency manifests are `package.json` and `package-lock.json`; update both when adding or changing packages.
