# Frameforge Portfolio

Full-stack Next.js + Supabase portfolio for Amit Prajapati.

## Local setup

1. Install Node.js 18+.
2. Run `npm install`.
3. Create a Supabase project.
4. In Supabase SQL Editor, run `supabase/schema.sql`.
5. Create an admin user in Supabase Authentication using `amitraj51015@gmail.com` and a password you choose.
6. Copy `.env.example` to `.env.local` and fill in Supabase values, service role key, Resend API key, and notification email.
7. Run `npm run dev`.
8. Open `/login` to access the private dashboard.

## Vercel deployment

1. Push this folder to GitHub.
2. Import the repository into Vercel.
3. Add every variable from `.env.example` in Vercel Project Settings → Environment Variables.
4. Deploy.
5. In Supabase Auth URL settings, add your Vercel URL as the Site URL and redirect URL if needed.

## Email

Create a Resend account and verify a sending domain for production. Set `RESEND_API_KEY`. The API route saves inquiries in Supabase and emails `NOTIFICATION_EMAIL`.

## Video uploads

The current dashboard stores video and thumbnail URLs, which is reliable for YouTube/Vimeo links. For direct file uploads, use the `portfolio` Supabase Storage bucket and add the resulting public URL in the dashboard. The storage policies are included in `supabase/schema.sql`.
