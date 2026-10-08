# CafeCraft — Cafe Management Dashboard

A role-based admin dashboard for managing a cafe's inventory, customer
complaints, and feedback — built as a mini-project exploring dashboard UI/UX
patterns with a modern React stack.

🔗 **Live Demo:** https://cafe-management-dashboard-beta.vercel.app/

## Features

- **Role-based login** — separate `cafe` and `admin` roles with distinct sessions
- **Overview dashboard** — at-a-glance stats: inventory health, pending
  complaints, average customer rating, low-stock alerts
- **Inventory management** — stock levels with progress indicators
  (critical/low/medium/good), category breakdown, and a stock-level bar chart
- **Customer care** — tabbed view of customer complaints (status + priority
  badges) and feedback (star ratings)
- Clean, responsive sidebar layout using shadcn/ui components
- Seamless experience with orders and inventory management. 
## Tech stack

`React` · `TypeScript` · `Vite` · `Tailwind CSS` · `shadcn/ui` (Radix
primitives) · `React Query` · `react-hook-form` + `zod` · `Recharts`

## Demo credentials

Login uses mock authentication (no real backend) — use either:

| Role  | Email             | Password  |
|-------|-------------------|-----------|
| Cafe  | `cafe@demo.com`   | `cafe123` |
| Admin | `admin@demo.com`  | `admin123`|

## Running locally

```sh
npm install
npm run dev
```
Then open the local URL Vite prints (usually `http://localhost:5173`).

## Important: this is a front-end prototype, not a production system

- **Data is mock/static.** Inventory, complaints, and feedback are hardcoded
  sample data (`src/data/mockData.ts`), not a live database. Login session is
  the only thing persisted, via `localStorage`.
- **"Add Item" on the Inventory page is UI-only** — it doesn't yet add a real
  item. It's there to show the intended interaction, not a finished feature.
- Authentication is a simulated check against hardcoded demo credentials, not
  a real auth system.

Treat this as a UI/UX and component-architecture reference, not a deployable
product as-is.

## Roadmap — what a real version would need

- A backend (FastAPI/Node/Express) with a real database for inventory,
  complaints, and feedback, replacing the static mock data
- Real authentication (hashed passwords, sessions/JWT) instead of hardcoded
  demo credentials
- Working CRUD — "Add Item," edit stock levels, update complaint status, etc.
- Role-based permissions enforced server-side, not just in the UI

## Deployment

This is a static Vite app — deployable for free on Vercel, Netlify, or GitHub
Pages. Once deployed, add the live link to the top of this README.
