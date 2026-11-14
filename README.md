# Naqaha - connect the real login and database (Supabase)

1. Create a free project at https://supabase.com
2. SQL Editor -> New query -> paste `supabase-setup.sql` -> Run.
3. Project Settings -> API: copy the Project URL and the `anon` public key.
   Open `naqaha.html`, find `const SB_URL='',SB_KEY='';` near the top of the script and paste them in.
   Never use the `service_role` key in this file.
4. Authentication -> URL Configuration: set Site URL to where the site runs (for example
   http://127.0.0.1:5500/naqaha.html with Live Server, or your hosted address) and add the same address
   under Redirect URLs. Password-reset and confirmation links return to this address.
5. Authentication -> Providers -> Email: choose whether new users must confirm their email.
   For real use set your own email sender (Authentication -> SMTP); the built-in sender is for testing only.
6. Run the page through Live Server or a web host, not by double-clicking the file.
