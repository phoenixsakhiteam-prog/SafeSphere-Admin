# SafeSphere Admin Dashboard

> Real-time women safety monitoring dashboard with live map, CCTV feed, and Supabase backend.

## Live Demo Setup

### Step 1 — Set Up Supabase
1. Create account at [supabase.com](https://supabase.com)
2. Create a new project
3. Go to **SQL Editor** → paste and run `supabase_schema.sql` (from the Backend repo)
4. Go to **Settings → API** → copy your:
   - **Project URL** (looks like `https://xxxx.supabase.co`)
   - **anon/public key**

### Step 2 — Configure index.html
Open `index.html` and edit lines at the top of the `<script>` block:

```js
const SUPABASE_URL      = "https://YOUR_PROJECT_ID.supabase.co";  // ← paste here
const SUPABASE_ANON_KEY = "YOUR_ANON_PUBLIC_KEY_HERE";             // ← paste here
```

### Step 3 — Open / Deploy
- **Local**: Just open `index.html` in any browser. No server needed.
- **GitHub Pages**: Push to a repo → Settings → Pages → Deploy from main branch
- **Netlify/Vercel**: Drag and drop the folder

## Features
- 📊 Real-time stats (total, active, resolved alerts)
- 🗺 Live map using Leaflet + OpenStreetMap (no API key needed)
- 📋 Alert detail panel with user info & emergency contacts
- ✅ Resolve alerts with one click
- 📷 Webcam CCTV simulation with snapshot
- 🔔 Supabase Realtime — instant push notifications for new alerts
- 📱 Responsive layout

## Tech Stack
| Component | Library |
|-----------|---------|
| Maps | [Leaflet.js](https://leafletjs.com) + OpenStreetMap |
| Database | [Supabase](https://supabase.com) (PostgreSQL) |
| Realtime | Supabase Realtime (WebSocket) |
| Camera | Browser `getUserMedia` API |
| Styling | Pure CSS (no frameworks) |
