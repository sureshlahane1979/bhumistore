# Bhumi Store

A responsive smartwatch and fitness wearable storefront built with React 19, TypeScript, Vite, Bootstrap 5, React Router and Context API. The storefront uses local demonstration data and remains usable without an API.

## Run locally

```sh
npm install
npm run dev
```

Create a `.env` file from `.env.example` to configure the future API:

```env
VITE_API_BASE_URL=http://localhost:5000/api
```

The Axios client is prepared in `src/services/api.ts`; mock product data currently powers the UI.

## Available routes

- `/` — storefront homepage
- `/shop` — product listing with category, price, brand, rating, search and sort controls
- `/product/:id` — product details, color selection and delivery estimate
- `/cart` and `/checkout` — local-storage cart and checkout demonstration (no payment is processed)
- `/login`, `/register`, `/forgot-password` — API-ready account forms
- `/account`, `/account/orders`, `/account/addresses`, `/account/wishlist`, `/account/password`
- `/about`, `/contact`, `/shipping`, `/faq`

Cart and wishlist state are saved in local storage. Account and checkout submission remain demonstration UI and do not claim to create an account, order or payment.

## Checks

```sh
npm run build
npm run lint
```

## Android readiness

Capacitor core and CLI are included in the project dependencies. The app uses standard React Router browser history and mobile-friendly layouts; install/configure the Capacitor platform when the Android wrapper is ready to be added.
