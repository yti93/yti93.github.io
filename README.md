# Publishing to GitHub Pages

1. Create a new GitHub repo named exactly `yti93.github.io` — this exact naming (under
   your account, github.com/yti93) gives you a root-level site at `https://yti93.github.io/`.
2. Copy all the files in this folder (`index.html`, `resume.html`, `talks.html`,
   `outside.html`, `style.css`, `images/`) into the repo.
3. Commit and push:
   ```
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/yti93/yti93.github.io.git
   git push -u origin main
   ```
4. In the repo on GitHub: Settings → Pages → Source → set to "Deploy from a branch", branch `main`, folder `/ (root)`. Save.
5. Your site will be live at `https://yti93.github.io/` within a minute or two.

## Adding a custom domain later

Once you buy a domain (Cloudflare/Namecheap):
- Add a `CNAME` file to the repo root containing just your domain, e.g. `youssefibrahim.com`
- In your DNS provider, add a CNAME record for `www` pointing to `yti93.github.io`, and either an ALIAS/ANAME record or the four GitHub Pages A records for the root domain (GitHub's docs list the current IPs).
- In GitHub Settings → Pages, enter the custom domain and enable "Enforce HTTPS" once it's verified.
