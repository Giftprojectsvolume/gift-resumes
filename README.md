# Gift Resumes — Frontend

## Setup

1. Run the three SQL migration files (schema → pricing → cost rates → this auth trigger) in your Supabase project's SQL editor, in that order, if you haven't already.
2. `npm install`
3. Copy `.env.example` to `.env` and fill in your Supabase project URL and anon key (found in Supabase → Project Settings → API).
4. `npm run dev` and open the local URL it prints.

## What's built so far

- Sign up (`/signup`) and sign in (`/login`), backed by Supabase Auth
- A logged-in-only `/dashboard` route (placeholder — built next)
- Mobile-first styling using the design tokens in `src/styles/tokens.css`

## Notes

- Supabase's default setting requires email confirmation before a new account can log in. If you'd rather skip that for early testing, it's a toggle in Supabase → Authentication → Providers → Email.
- The `handle_new_user` trigger (separate SQL file) must be run once, or new sign-ups will have no matching row in `profiles`.
