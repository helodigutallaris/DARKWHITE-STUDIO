DARKWHITE STUDIO — MULTI-USER PWA STARTER
==========================================

File:
- index.html: PWA UI, login/sign-up, profile name, dual-currency transactions
- config.js: Supabase project URL + publishable/anon key placeholders
- supabase-schema.sql: database tables and row-level security policies
- manifest.json, service-worker.js, icons/: PWA installation files

IMPORTANT:
This starter is not ready for production until Supabase is configured and SQL is run.
Never add a Supabase service_role/secret key to browser code. Only the publishable/anon key is suitable here.
Each user’s profile and transactions are protected by RLS and user_id ownership policies.
PWA icon/name is shared in this static deployment. Dashboard studio name is per account. Per-user installed icon/name cannot be reliably customized from one shared static manifest.

SETUP
1. Create a free project at https://supabase.com/ and wait until ready.
2. In Supabase, open SQL Editor > New query, paste supabase-schema.sql and Run.
3. In Project Settings / API (or Connect), copy Project URL and publishable/anon key.
4. Edit config.js and replace both placeholder strings. Do not share your key in chat.
5. In Supabase Authentication > URL Configuration, add your GitHub Pages URL to Site URL and Redirect URLs:
   https://helodigutallaris.github.io/DARKWHITE-STUDIO/
6. In Authentication settings, decide whether email confirmation is required. If enabled, users need to confirm their email before signing in.
7. In GitHub repository helodigutallaris/DARKWHITE-STUDIO, upload/replace these files in repository root:
   index.html, config.js, manifest.json, service-worker.js, supabase-schema.sql, and icons/ folder.
   Keep the repository public because this is GitHub Pages. Do not put private financial exports in the repository.
8. Wait for GitHub Pages deployment, open the website and test sign-up with an account you control.
9. Test with a second test account. Confirm each account only sees its own transactions.

INSTALL
- iPhone/iPad: open the website in Safari > Share > Add to Home Screen.
- Android: open the website in Chrome > menu > Install app/Add to Home screen.

KNOWN LIMITATIONS
- Studio name is per account, but app icon/title is global for this single PWA deployment.
- Data requires internet for sign-in and cloud transactions; cached app shell may load offline but database actions will not work offline.
- This is a starter implementation. Before real commercial use, add stronger validation, password reset flow, backups, and testing.
