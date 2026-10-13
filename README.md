# Chesterfield Community Church — PWA Dashboard

A mobile-first Progressive Web App (PWA) dashboard created from the **Living Grace Sanctuary** design system in Google Stitch.

---

## 📱 Features

- **PWA Ready**: Installable on iOS, Android, and Desktop with offline caching via Service Worker (`sw.js`) and Web App Manifest (`manifest.json`).
- **Sunday Gathering & Livestream Hub**: Highlights morning Bible Study (9:30 AM), Worship Service (10:30 AM), nursery/kids notes, and 1-tap YouTube livestream launcher.
- **Prayer Request Modal**: Interactive confidential prayer request bottom sheet.
- **Church Hub Actions**: Rapid navigation for livestreams, instant member directory, youth programs, and volunteer scheduling.
- **Ministries Showcase**: Highlights Discovery Kids, small groups/fellowship, and seasonal community events (e.g. FallThanksMas).
- **Interactive Map & Directions**: Quick location access to 123 Linden Ln, Chesterfield, IN.
- **Office Hours & Direct Contact**: Click-to-call and click-to-email shortcuts with scheduled operating hours.

---

## 🎨 Design System

- **Theme**: Living Grace Sanctuary
- **Primary Color**: Deep Sapphire (`#00288E` / `#1E40AF`)
- **Accent Color**: Radiant Flame Amber (`#F59E0B` / `#D97706`)
- **Canvas Color**: Off-White Sanctuary Slate (`#F7F9FB`)
- **Typography**: Plus Jakarta Sans (Headings) & Inter (Body & Labels)

---

## 🚀 Local Development

You can run the dashboard locally with any static server:

```bash
# Using Node / npx
npx serve .

# Or using Python (if installed)
python -m http.server 8080
```

---

## ⛅ Cloudflare Deployment

### Option 1: Direct Deploy via Wrangler CLI
```bash
# 1. Login to Cloudflare
npx wrangler login

# 2. Deploy to Cloudflare Pages
npx wrangler pages deploy . --project-name=church-pwa-dashboard
```

### Option 2: Cloudflare Pages Git Integration (Recommended)
1. Go to the [Cloudflare Dashboard](https://dash.cloudflare.com/)
2. Navigate to **Workers & Pages** > **Create application** > **Pages** > **Connect to Git**
3. Select the repository: `humangeek77-star/church-pwa-dashboard`
4. Set build settings:
   - **Framework preset**: None
   - **Build command**: (leave empty)
   - **Build output directory**: `.`
5. Click **Save and Deploy**. Any subsequent push to `main` will automatically build and publish.

### Option 3: GitHub Actions
A workflow is preconfigured in `.github/workflows/deploy.yml`. Add your Cloudflare credentials to GitHub Secrets:
- `CLOUDFLARE_API_TOKEN`
- `CLOUDFLARE_ACCOUNT_ID`
