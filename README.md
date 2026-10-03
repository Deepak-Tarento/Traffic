# Aurion — Website

A fast, responsive, multi-page static website for **Aurion** (auriontechdata.com),
built with the same information architecture as a traffic-data company site and a subtle
light-blue theme. Pure HTML/CSS/JS — no build step, no dependencies — so it deploys to any
static host with automatic HTTPS.

## Pages
- `index.html` — Home (hero, who-we-are, services, stats, process, testimonial, CTA)
- `services.html` — Traffic Data Count · Software Development
- `about.html` — About Us
- `our-story.html` — Company timeline
- `insight.html` — Articles / blog grid
- `reports.html` — Sample deliverables
- `careers.html` — Open roles
- `contact.html` — Contact form + map

## Structure
```
Traffic/
├── index.html + 7 other pages
├── css/style.css      # theme + all layout (light-blue palette in :root)
├── js/main.js         # nav, scroll reveal, form demo
├── assets/logo.svg    # original brand mark
└── README.md
```

## Preview locally
```bash
cd /Users/deepakkumar/Desktop/Traffic
python3 -m http.server 8080
# open http://localhost:8080
```

## Deploy over HTTPS (pick one — all give free HTTPS)

**Netlify (drag & drop)**
1. Go to https://app.netlify.com/drop
2. Drag the whole `Traffic` folder onto the page.
3. You get a live `https://…netlify.app` URL instantly. Add your `auriontechdata.com`
   domain under Site settings → Domain management (HTTPS is provisioned automatically).

**GitHub Pages**
```bash
cd /Users/deepakkumar/Desktop/Traffic
git init && git add . && git commit -m "Aurion site"
gh repo create aurion --public --source=. --push
```
Then in the repo: Settings → Pages → deploy from `main` / root. Served over HTTPS at
`https://<user>.github.io/aurion/`.

**Vercel:** `npx vercel` in this folder, follow the prompts.

**Cloudflare Pages:** connect the repo or upload the folder — free HTTPS + CDN.

## Customising
- **Colors:** edit the `--blue-*` variables at the top of `css/style.css`.
- **Contact/phone/email:** search-replace `info@auriontechdata.com`, `+91 7814270306`,
  and the Bangalore address across the HTML files.
- **Contact form:** currently a front-end demo. To actually receive messages, point the
  `<form>` at a service like Formspree/Netlify Forms, or your own endpoint.
- **Logo:** replace `assets/logo.svg` with your own.

## Notes
This is an original, independently-authored implementation (original logo, original copy)
inspired by a traffic-data company layout — not a copy of any third party's proprietary
assets.
