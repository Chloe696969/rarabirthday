# Pelabirthday 💌

A responsive, four-section birthday letter website built with Next.js, Tailwind CSS v4, TypeScript, and Framer Motion. Ready for Vercel.

## Sections
1. **Today is your day** — hero, birthday date, and navigation.
2. **Birthday Girl** — a celebratory introduction.
3. **My Favorite Person** — birthday wishes from the original Canva design.
4. **Birthday Letter** — personal note from Satria plus a customizable photo gallery.

The exact wording retrieved from the Canva design is preserved where available. Canva's visual assets are not automatically exported by this project, so replace the gallery placeholders with your own images.

## Run locally

Requires Node.js 20.9+.

```bash
npm install
npm run dev
```

Open http://localhost:3000.

To verify production build:

```bash
npm run build
npm start
```

## Customize the content

Edit `src/config/site.ts`:
- recipient name and birthday date
- page headings and birthday wishes
- the short letter
- gallery image paths and captions

Put gallery photos in `public/images/` and reference them with paths such as `/images/photo-1.jpg`.

## Add background music

Put an audio file named **`birthday.mp3`** in `public/music/`.

The player uses `/music/birthday.mp3`. Autoplay is attempted on first load, but browsers—especially mobile browsers—often block autoplay with sound. If blocked, the floating music control shows a play button; the visitor can tap it to start playback. This is a browser policy and cannot be reliably bypassed by website code.

Use music you have permission to publish. Keep the file reasonably compressed for mobile visitors.

## Deploy to Vercel

### GitHub flow
1. Create a new empty GitHub repository.
2. Upload/push this project's files to the repository (do not upload `node_modules`).
3. In Vercel, choose **Add New → Project**, import that repository, and deploy. Vercel detects Next.js automatically.

### CLI flow
```bash
npm i -g vercel
vercel
vercel --prod
```

No environment variables are required for the basic site.

## Important
- `public/music/birthday.mp3` is intentionally a placeholder path; add your own audio file locally before deployment.
- `public/images/` contains instructions/placeholders, not the private photos from Canva.
- The Canva connection provided text and metadata, but not a complete editable export of all visual assets. The website is a visual reconstruction, not a pixel-perfect automated conversion.
