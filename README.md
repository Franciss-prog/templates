# templates

Personal collection of starter templates. Grab one, clone, `.env`, build.

## sveltekit — Auth-Ready SaaS Starter

Drop-in SvelteKit starter for SaaS projects. Goal: clone it, fill `.env`, start building features — no auth wiring, no boilerplate.

### Stack

- SvelteKit 2 + Svelte 5
- TailwindCSS v4 (`@tailwindcss/vite`, forms + typography plugins)
- TypeScript
- ESLint + Prettier (with Svelte/Tailwind plugins)
- Vitest (unit + browser via Playwright)
- `adapter-vercel` — deploy-ready out of the box

### Status

Base scaffold in place (SvelteKit, Tailwind v4, lint/format/test tooling, Vercel adapter). Auth and DB layer not wired yet.

### Roadmap

- [ ] Auth system (working out of the box)
- [ ] NeonDB integration + connection config (`DATABASE_URL`)
- [ ] Database schema for users/auth
- [ ] Protected routes + session handling
- [ ] Env-based config (`DATABASE_URL`, auth secrets, ...)
- [ ] OAuth providers (Google, GitHub) — optional
- [ ] Email/password auth toggle — optional
- [ ] Basic dashboard layout — optional
- [ ] Example CRUD module — optional

### Getting started

```bash
cd sveltekit
bun install
cp .env.example .env   # once auth/DB land — fill DATABASE_URL + auth secrets
bun run dev
```

### Scripts

| Command | What it does |
|---|---|
| `bun run dev` | start dev server |
| `bun run build` | production build |
| `bun run preview` | preview production build |
| `bun run check` | type-check (svelte-check) |
| `bun run lint` | prettier + eslint check |
| `bun run format` | prettier write |
| `bun run test` | run unit tests once |
