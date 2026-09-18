# Porter & Co. Plumbing

Single-page marketing site for Porter & Co. Plumbing, Tulsa, OK.

- `index.html` holds the whole site (home, services, about, contact, privacy)
  with no build step and no dependencies beyond Google Fonts.
- `images/` holds photos. See `images/README.md` for the filenames the page
  looks for.
- `admin/index.html` is the office admin dashboard (schedule and dispatch,
  jobs, customers, estimates, invoices and accounts receivable, reports,
  staff, equipment and fleet, inventory, settings). It runs entirely on mock
  data in the browser today; Supabase, Resend, and Vercel are the planned
  backend. It is not linked from the public site and is served at
  `/admin/`.
- `.github/workflows/pages.yml` publishes the site to GitHub Pages on every
  push to `main`.

## Going live

1. In the repository settings open **Pages** and set **Source** to
   **GitHub Actions** (one-time step).
2. Merge to `main`. The workflow deploys to
   https://futurexrp.github.io/PorterWebsite/ within a minute or two.

To use a custom domain, add it under **Settings → Pages → Custom domain**
and point the domain's DNS at GitHub Pages.

## Admin dashboard

Open https://futurexrp.github.io/PorterWebsite/admin/ and sign in with any
email and password (the gate is a placeholder until Supabase auth exists).
Everything you add or change lives in memory for that browser tab only.

Planned wiring, in order:

1. **Supabase**: tables for customers, jobs, estimates, invoices, payments,
   staff, vehicles, tools, inventory; auth with admin, office, and technician
   roles; row-level security so techs see only their own schedule.
2. **Resend**: estimate and invoice emails, payment receipts, overdue
   reminders. Every "send" button in the dashboard already marks where a call
   goes.
3. **Vercel**: hosting for both the public site and the admin app, with
   preview deploys per branch and environment variables for the two services
   above.

## Editing

Open `index.html` in any editor. Phone number, hours, address, and license
number appear in a few places each, so search the file when changing them.
