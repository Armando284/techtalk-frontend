# TechTalk Frontend

This is the frontend for the TechTalk platform, a social platform for developers. It is built using React and Vite, providing a fast and modern interface for user interaction with the backend API.

## Requirements

- Node.js (v14 or higher)
- npm (v6 or higher)

## Setup

### 1. Clone the repository

```bash
git clone https://github.com/your-username/techtalk-frontend.git
cd techtalk-frontend
```

### 2. Install dependencies

```bash
npm install
```

### 3. Create a `.env` file

Create a `.env` file in the root directory with the following contents:

```
VITE_API_URL=http://localhost:3000/api
```

Make sure to replace `http://localhost:3000/api` with your backend API URL if it’s different.

### 4. Run the development server

```bash
npm run dev
```

This will start the frontend on `http://localhost:5173` (or another port if specified by Vite).

## Build for production

To create a production build, run:

```bash
npm run build
```

The production-ready files will be generated in the `dist` directory.

## Deployment

To deploy the frontend, upload the contents of the `dist` directory to your hosting service. For services like Vercel or Netlify, simply connect the repository, and the service will handle the build and deployment.

## Scripts

- `npm run dev`: Start the development server.
- `npm run build`: Build the project for production.
- `npm run preview`: Preview the production build locally.

## License

This project is licensed under the MIT License.

---

# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
export default tseslint.config({
  languageOptions: {
    // other options...
    parserOptions: {
      project: ['./tsconfig.node.json', './tsconfig.app.json'],
      tsconfigRootDir: import.meta.dirname,
    },
  },
})
```

- Replace `tseslint.configs.recommended` to `tseslint.configs.recommendedTypeChecked` or `tseslint.configs.strictTypeChecked`
- Optionally add `...tseslint.configs.stylisticTypeChecked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and update the config:

```js
// eslint.config.js
import react from 'eslint-plugin-react'

export default tseslint.config({
  // Set the react version
  settings: { react: { version: '18.3' } },
  plugins: {
    // Add the react plugin
    react,
  },
  rules: {
    // other rules...
    // Enable its recommended rules
    ...react.configs.recommended.rules,
    ...react.configs['jsx-runtime'].rules,
  },
})
```
