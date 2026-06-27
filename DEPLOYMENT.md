# Deployment Instructions for Vercel

## What Was Changed

### 1. Event Updates
- **Engagement Ceremony** - Remains unchanged (St Joseph's church, Devagiri Calicut)
- **Wedding Ceremony** - Added as separate event
  - Venue: St. Simon's Jacobite Syrian Orthodox Church, Velloor
  - Time: 11:00 AM on August 30, 2026
  - Map: https://maps.app.goo.gl/QofZw1hVm1RzJtxk8?g_st=ic

- **Wedding Reception** - Updated as separate event
  - Venue: St. John's Orthodox Cathedral Pampady
  - Time: 01:00 PM on August 30, 2026
  - Map: https://maps.app.goo.gl/gnN31NgC99bSOCV8

### 2. Link Preview (Social Media Sharing)
- Added Open Graph meta tags for Facebook, WhatsApp, LinkedIn
- Added Twitter Card meta tags
- Preview image: `/assets/link-preview.jpeg` (the uploaded "Save the Date" image)
- When shared, the link will display the couple's photo with wedding details

## Deploy to Vercel

### Option 1: Vercel CLI (Recommended)

1. Install Vercel CLI globally (if not already installed):
   ```bash
   npm install -g vercel
   ```

2. Navigate to project directory:
   ```bash
   cd /Users/abhinand/Documents/Codex/2026-06-18/files-mentioned-by-the-user-rec
   ```

3. Deploy:
   ```bash
   vercel
   ```

4. Follow the prompts:
   - Set up and deploy? **Y**
   - Which scope? Select your account
   - Link to existing project? **N** (unless you want to link to existing)
   - What's your project's name? **jewel-merin-wedding** (or your choice)
   - In which directory is your code located? **./** (press Enter)
   - Want to override the settings? **N**

5. For production deployment:
   ```bash
   vercel --prod
   ```

### Option 2: Vercel Dashboard (Web Interface)

1. Go to [vercel.com](https://vercel.com) and sign in
2. Click "Add New Project"
3. Import from Git repository OR upload the folder
4. Configure:
   - Framework Preset: **Vite**
   - Build Command: `npm run build`
   - Output Directory: `dist`
   - Install Command: `npm install`
5. Click "Deploy"

### Option 3: GitHub Integration

1. Push this code to a GitHub repository
2. Go to [vercel.com](https://vercel.com)
3. Click "Import Project"
4. Select your GitHub repository
5. Vercel will auto-detect Vite settings
6. Click "Deploy"

## After Deployment

1. **Update the Open Graph URL**: 
   - Edit `index.html` line with `<meta property="og:url" content="..."/>`
   - Replace `https://yourdomain.com` with your actual Vercel URL

2. **Test Link Preview**:
   - Share your link on WhatsApp, Facebook, or Twitter
   - The "Save the Date" image should appear with couple details

3. **Custom Domain (Optional)**:
   - In Vercel dashboard, go to Settings > Domains
   - Add your custom domain

## Project Structure

```
.
├── index.html              # Updated with meta tags for link preview
├── package.json
├── vercel.json            # SPA routing configuration
├── vite.config.js
├── src/
│   ├── App.jsx            # Updated with 3 events
│   ├── main.jsx
│   └── styles.css
└── public/
    └── assets/
        ├── link-preview.jpeg    # Social media preview image
        ├── hero.jpeg
        ├── couple.jpeg
        ├── ceremony.jpeg
        ├── gallery-*.jpeg
        └── invitation-melody.wav
```

## Testing Locally

```bash
# Development mode
npm run dev

# Build and preview
npm run build
npm run preview
```

## Important Notes

- All images must be in `/public/assets/` folder
- The `link-preview.jpeg` file must exist in `/public/assets/`
- Build was tested and completed successfully ✓
- No breaking changes were made to the existing functionality
- The project is production-ready

## Support

If you encounter issues:
1. Ensure all image files are present in `public/assets/`
2. Run `npm install` to ensure dependencies are installed
3. Run `npm run build` to test local build
4. Check Vercel build logs if deployment fails
