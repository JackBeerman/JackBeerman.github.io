# jackbeerman.github.io

Personal research site. One static page (`index.html`) with no build step.

## Deploy on GitHub Pages

1. Create a public repo named exactly `JackBeerman.github.io`.
2. From this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/JackBeerman/JackBeerman.github.io.git
   git push -u origin main
   ```
3. Repo **Settings → Pages**: Source = *Deploy from a branch*, Branch = `main` / `(root)`.
4. The site goes live at https://jackbeerman.github.io within a minute or two.

## Custom domain (optional)

1. Buy a domain (e.g. `jackbeerman.com`).
2. Repo **Settings → Pages → Custom domain**: enter it. GitHub adds a `CNAME` file.
3. At your registrar, add DNS records:
   - `A` records for `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` for `www` → `jackbeerman.github.io`
4. Tick **Enforce HTTPS** once the certificate is issued.
5. Update the `canonical`, `og:url` and JSON-LD `url` in `index.html` to the new domain.

## Editing

- **New paper:** copy an `<li>` in the Publications section.
- **New project:** copy an `<article class="project">` block.
- **Colors:** tokens are at the top of the `<style>` block (light theme, then dark).
