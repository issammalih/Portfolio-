# Issam Malyh portfolio

Static site for GitHub Pages: `index.html` + `assets/`.

## Edit your details
Open `index.html`, search for "Edit your details here" (`CONFIG`): email, LinkedIn, calendar link, `formKey`.

## Security checklist
- The page ships a strict Content-Security-Policy: only its own scripts run, and data can only be sent to formsubmit.co.
- Form + chatbot: hidden honeypot field, 4-second bot timer, max 3 requests per hour per visitor, length limits, link-spam filter, all user text escaped (no HTML injection).
- After the first test request, FormSubmit emails you an activation link. Click it, then copy the random alias FormSubmit gives you into `CONFIG.formKey` so your email is not exposed to bots.
- Never put API keys (OpenAI etc.) in this repo. A real AI brain must run in a Cloudflare Worker that keeps the key secret.
- GitHub: turn on 2FA, Settings > Pages > "Enforce HTTPS", and only you as collaborator.
