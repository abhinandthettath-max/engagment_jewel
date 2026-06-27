# Wedding Invitation Website

A beautiful, interactive wedding invitation website built with React and Vite.

## 🎉 Features

- ✨ **Elegant Intro Animation** - Full-screen cover with slide-up reveal
- ⏰ **Live Countdown Timer** - Real-time countdown to the engagement
- 🎵 **Background Music** - Auto-playing invitation melody with toggle control
- 📍 **3 Events with Locations**:
  - Engagement Ceremony (Aug 24, 2026)
  - Wedding Ceremony (Aug 30, 2026)
  - Wedding Reception (Aug 30, 2026)
- 🗺️ **Google Maps Integration** - Direct links to all venues
- 📸 **Photo Gallery** - Polaroid-style sticky scroll gallery
- 📱 **Fully Responsive** - Optimized for mobile and desktop
- 🔗 **Social Media Preview** - Beautiful link previews when shared

## 🚀 Quick Start

### Development
```bash
npm install
npm run dev
```

### Build
```bash
npm run build
```

### Preview Build
```bash
npm run preview
```

## 📦 Deployment

This project is ready for immediate deployment to Vercel.

**See [DEPLOYMENT.md](./DEPLOYMENT.md) for detailed deployment instructions.**

Quick deploy:
```bash
npm install -g vercel
vercel
```

## 🎨 Customization

All event details are configured in `src/App.jsx`:

```javascript
const events = [
  {
    title: "Engagement Ceremony",
    date: "Monday, August 24, 2026",
    time: "04:00 PM",
    venue: "St Joseph's church, Devagiri Calicut, Kerala",
    map: "https://maps.app.goo.gl/...",
  },
  // ... more events
];
```

## 📂 Project Structure

```
.
├── index.html              # Main HTML with meta tags
├── package.json
├── vercel.json            # Vercel deployment config
├── vite.config.js
├── src/
│   ├── App.jsx            # Main React component
│   ├── main.jsx           # React entry point
│   └── styles.css         # All styles
└── public/
    └── assets/
        ├── link-preview.jpeg    ✓ Exists (85KB)
        ├── hero.jpeg
        ├── couple.jpeg
        ├── ceremony.jpeg
        ├── gallery-*.jpeg
        └── invitation-melody.wav
```

## ✅ Build Status

- **Build:** ✅ Successful (639ms)
- **Output Size:** 204.37 KB JS (64.58 KB gzipped)
- **CSS Size:** 13.06 KB (3.82 KB gzipped)
- **Link Preview Image:** ✅ Present (85 KB)
- **Vercel Ready:** ✅ Yes


## 🛠️ Tech Stack

- **React 19** - Latest React version
- **Vite 7** - Lightning-fast build tool
- **Lucide React** - Beautiful icons
- **CSS3** - Custom animations and styling
- **Google Fonts** - Elegant typography (Cormorant Garamond, Great Vibes, Lora)

## 📄 Documentation

- **[DEPLOYMENT.md](./DEPLOYMENT.md)** - Complete deployment guide
- **[CHANGES.md](./CHANGES.md)** - Detailed changelog

## 🎨 Design Features

- Warm color palette (cream, gold, paper white)
- Elegant script and serif typography
- Smooth scroll-triggered animations
- Glassmorphism effects on floating controls
- Polaroid-style photo gallery
- Responsive design (mobile-first)

## ⚠️ Post-Deployment

After deploying, update the Open Graph URL in `index.html`:

```html
<meta property="og:url" content="YOUR_ACTUAL_VERCEL_URL" />
```

Replace `https://yourdomain.com` with your actual deployment URL.

## 📝 License

Private project - All rights reserved


