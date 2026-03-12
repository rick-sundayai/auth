# Next.js + Supabase Auth Template

Next.js 15, Supabase, TypeScript, Tailwind CSS. Login, register, password reset, protected routes, user profiles.

## Setup

**1. Install**
```bash
npm install
```

**2. Environment**
```bash
cp .env.example .env.local
```

```env
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
NEXT_PUBLIC_APP_URL=http://localhost:3000
```

**3. Database** — run `database/setup.sql` in your Supabase SQL editor.

**4. Run**
```bash
npm run dev
```

## Project Structure

```
src/
├── app/
│   ├── auth/           # login, register, reset-password
│   ├── dashboard/      # protected page (server component)
│   ├── layout.tsx
│   └── page.tsx
├── components/
│   ├── auth/           # LoginForm, RegisterForm
│   └── dashboard/      # DashboardClient
├── hooks/useAuth.tsx
├── lib/
│   ├── auth/           # AuthService
│   ├── supabase/       # client + server clients
│   ├── types/auth.ts
│   └── validation/     # Zod schemas
└── middleware.ts
```

## Scripts

```bash
npm run dev
npm run build
npm run type-check
npm run lint
```

## Deployment

Deploy to Vercel and set environment variables:

```env
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
NEXT_PUBLIC_APP_URL=https://yourdomain.com
```

## License

MIT
