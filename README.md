# CTF Challenge — Static traces

**Category:** Web  
**Difficulty:** Beginner  
**Concept:** View source — flag split across HTML, CSS, and JavaScript comments

---

## Challenge description

A boring maintenance page. Nothing to click. Maybe the deployment team left something in the assets.

---

## Run locally

Open `index.html` in a browser, or from this folder:

```bash
cd web/chal2
npx --yes serve .
```

---

## GitHub Pages + `plain.crypton-club.xyz`

1. Push this repository to GitHub (already connected if you cloned from the org/user remote).
2. In the repo on GitHub: **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose **`main`** and **`/ (root)`**, then **Save**.
4. Under **Custom domain**, enter **`plain.crypton-club.xyz`** and save (GitHub may add the `CNAME` file automatically; this repo already includes one).
5. In your DNS for `crypton-club.xyz`, add a **CNAME** record:
   - **Name / host:** `plain`
   - **Target / value:** `<your-github-username>.github.io`
6. Wait for DNS and the certificate check to finish (can take a few minutes).

---

## Solve (organizers)

The flag is split into three comments:

- `index.html` (HTML comment)
- `style.css` (CSS comment)
- `app.js` (JavaScript comment)

**Flag:** `flag{static_traces_are_everywhere}`
