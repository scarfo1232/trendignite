# TrendIgnite Website v2

A production-style Next.js landing page for TrendIgnite.

## Offer used
- $3,000/month management
- $3,000/month minimum ad spend
- HVAC growth + customer acquisition
- Paid advertising, content direction, lead follow-up system and reporting

## Contact form
The production form sends website enquiries to:

`jaydenndlovu821@gmail.com`

It uses Resend from a server-side Next.js route, so the API key is **not** exposed to visitors.

## Deploy on Vercel

1. Create a GitHub repository and upload this folder.
2. Import the repository into Vercel.
3. In Vercel → Project → Settings → Environment Variables add:
   - `RESEND_API_KEY`
   - `TRENDIGNITE_CONTACT_EMAIL` = `jaydenndlovu821@gmail.com`
   - `TRENDIGNITE_FROM_EMAIL` = `TrendIgnite <hello@YOUR-DOMAIN.com>`
4. In Resend, verify the domain you will use for the `FROM` address.
5. Redeploy.
6. Submit the website form and confirm the message arrives at the Gmail inbox.

### Testing before you own a domain
Resend provides a development sender, but production sending is best done from a domain you have verified. Do not put `RESEND_API_KEY` in any `NEXT_PUBLIC_` variable.

## Run locally

```bash
npm install
cp .env.example .env.local
npm run dev
```

Open http://localhost:3000

## Before publishing publicly
- Connect your final domain.
- Add privacy policy and terms pages.
- Add your legal/trading business details as appropriate.
- Add analytics and ad conversion tracking only after configuring consent/privacy correctly.
- Do not add fake case studies or performance claims.
- Replace the current discovery CTA with a booking URL later if you adopt one.

## Files
- `app/page.js` — website
- `app/globals.css` — design
- `components/ContactForm.js` — lead form
- `app/api/contact/route.js` — sends enquiries to Gmail through Resend
- `.env.example` — environment variable template
