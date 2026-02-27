# HH Crowd Proxy

Kleiner Vercel-Proxy für die Hamburger Passanten-API (CORS-Fix).

## Deploy in 3 Schritten

### 1. Vercel CLI installieren
```bash
npm install -g vercel
```

### 2. In diesen Ordner wechseln & deployen
```bash
cd hh-crowd-proxy
vercel
```
Vercel fragt ein paar Dinge:
- "Set up and deploy?" → **Y**
- "Which scope?" → dein Account wählen
- "Link to existing project?" → **N**
- "Project name?" → z.B. `hh-crowd-proxy`
- "In which directory is your code?" → **.** (Enter)

### 3. Deine Proxy-URL notieren
Nach dem Deploy zeigt Vercel dir eine URL wie:
```
https://hh-crowd-proxy-xyz.vercel.app
```
Dein API-Endpunkt ist dann:
```
https://hh-crowd-proxy-xyz.vercel.app/api/crowd
```

## In der HTML-App eintragen
In `hh_crowd_radar.html` die Zeile mit `PROXY_URL` ändern:
```javascript
const PROXY_URL = "https://hh-crowd-proxy-xyz.vercel.app/api/crowd";
```
