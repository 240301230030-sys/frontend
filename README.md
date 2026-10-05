# MotherCare

MotherCare is a pregnancy wellness dashboard with a local Node.js API for demo profile, caregiver, doctor, health summary, report, and assistant flows.

## Run locally

Use Node.js 20 or newer. Start the API and frontend in separate terminals from the project directory:

```sh
npm run server
npm run dev
```

Vite proxies `/api` requests to `http://localhost:3001`. Check the API at `/api/health`.

## Data and scope

On first start, the API seeds `server/data/store.json` from demo data. Profile, family, and doctor updates are persisted there. This local file should not be committed or used for real patient information.

Report share attempts are recorded locally and return `delivered: false`; no notification provider is configured. Health values and assistant behavior are demo-only. The backend has no authentication, authorization, encryption, or production-grade database and is not suitable for clinical data.

## Checks

```sh
npm run lint
npm run build
```

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Oxc](https://oxc.rs)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/)

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.
