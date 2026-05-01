# 6b74.dev — landing page

Personal landing page / digital business card for tonk.

## Setup

1. Drop `index.html` into a new GitHub repo (e.g., `crimsonpistil/6b74.dev` or `crimsonpistil.github.io`)
2. Add your photo as `me.jpg` (or any name) to the repo root
3. In `index.html`, find the line marked with the swap-photo comment near line 152 and replace:
   ```html
   <span class="placeholder">tonk</span>
   ```
   with:
   ```html
   <img src="me.jpg" alt="tonk">
   ```
4. Add a `CNAME` file containing: `6b74.dev`
5. In Cloudflare DNS, add four A records pointing to GitHub Pages:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
   - All on name `@`, all with proxy OFF (gray cloud)
6. In your repo's GitHub Pages settings, set custom domain to `6b74.dev`
7. Wait for DNS check + TLS cert provisioning, then enable Enforce HTTPS

## Customization

- All design tokens are CSS variables at the top of the `<style>` block — palette borrowed from the hunt reference for visual family continuity
- Project cards: copy the `<a class="project">` block to add new projects
- Status pills: `status-live`, `status-dev`, `status-idea` (different colors)
- Mobile-responsive at 540px breakpoint
- No frameworks, no build step, no JavaScript
- Single file, system fonts, loads in <100ms

## Easter egg

The footer contains the hex decode of `6b74 = kt` with a tooltip on hover showing the ASCII hex breakdown (`6B = 'k', 74 = 't' in ASCII hex`).

## License

MIT or whatever feels right — it's your site.
