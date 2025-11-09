# CoachRoom (AI Interview Mocker)

>A small, modern Next.js app for practicing mock interviews using AI and recorded answers.

This repository uses Next.js (app router), Tailwind CSS, Clerk for auth, Drizzle ORM for database access, and Google Generative AI for interview question generation. It ships with helper components and a minimal client/server structure.

## Quick start

Prerequisites
- Node.js 18+ (or the version compatible with Next.js 14+)
- A Postgres-compatible database (Neon, Supabase, etc.) and connection URL
- A Clerk account (or replace authentication as needed)
- Credentials for any AI provider used (Google Generative AI or similar)

Install dependencies

```powershell
npm install
```

Run development server

```powershell
npm run dev
```

Build for production

```powershell
npm run build
npm run start
```

Useful scripts
- `npm run dev` — start Next.js in development
- `npm run build` — build for production
- `npm run start` — start production server (after build)
- `npm run lint` — run Next.js linter
- `npm run db:push` — push Drizzle migrations (uses `drizzle-kit`)
- `npm run db:studio` — open Drizzle Studio

## Environment variables

This project relies on a few external services. Add these (or equivalents) to a `.env.local` file at the project root:

- Database connection: set a `DATABASE_URL` (or whatever your database/adapter expects). This is required for Drizzle ORM.
- Clerk / Auth: create a Clerk app and set the required Clerk environment variables according to Clerk's docs (publishable key, secret, frontend API values). Do not commit these to source control.
- AI provider credentials: if you use Google Generative AI or another provider, follow their docs and set the credentials required to call the service.

Example `.env.local` (values are placeholders — check provider docs):

```
# .env.local (example)
DATABASE_URL="postgresql://username:password@hostname:5432/dbname"
# Clerk / Auth variables — set per Clerk docs
# AI provider credentials — set per provider docs
```

## Project structure (high level)

- `app/` — Next.js App Router pages and server/client components
  - `app/dashboard/` — protected dashboard and components
- `components/` — reusable UI components
- `utils/` — helpers like `db.js`, `schema.js`, and AI modal helpers
- `drizzle/` — SQL migrations and snapshots

  DEMO LINK
  https://intelli-mock-rbok.vercel.app/

## Below are a couple of screenshots from the app.
Login screen

![Login](/public/login.png)

Dashboard

![Dashboard](/public/Dashboard.png)
