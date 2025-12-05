# Mac — 3D Product Page (React, Vite, Three.js, GSAP)

A modern, animated product experience inspired by Apple's Mac pages. Built with React 19, Vite, Three.js via `@react-three/fiber`, smooth scroll/entrance animations with GSAP + ScrollTrigger, and utility-first styling powered by Tailwind CSS v4. State is managed with `zustand` and responsive behavior via `react-responsive`.

https://github.com/ — live demo link (optional). Replace with your deployment URL.

---

## ✨ Features
- 3D Macbook model viewer using `three` + `@react-three/fiber` and helpers from `@react-three/drei`
- Scroll-driven sections and parallax effects with GSAP `ScrollTrigger`
- Responsive layout with mobile optimizations (e.g., conditional animations)
- Lightweight state management with `zustand`
- Fast dev/build pipeline with Vite
- Accessible, keyboard-friendly navigation skeleton

## 🧱 Tech Stack
- React 19 + Vite 7
- Three.js, @react-three/fiber, @react-three/drei
- GSAP + @gsap/react (ScrollTrigger registered in `src/App.jsx`)
- Tailwind CSS v4 via `@tailwindcss/vite`
- Zustand for global store
- clsx for conditional class composition

## 📁 Key Structure
```
D:/koulis/Desktop/Mac
├─ public/                       # Static assets (icons, logo, etc.)
├─ src/
│  ├─ components/
│  │  ├─ NavBar.jsx             # Top navigation
│  │  ├─ Hero.jsx               # Landing hero (intro)
│  │  ├─ ProductViewer.jsx      # 3D Macbook viewer
│  │  ├─ Showcase.jsx           # Product showcase section
│  │  ├─ Performance.jsx        # GSAP-driven performance visuals
│  │  ├─ Features.jsx           # Feature highlights
│  │  ├─ Highlights.jsx         # More highlights/details
│  │  ├─ Footer.jsx             # Footer
│  │  └─ models/
│  │     ├─ Macbook.jsx         # 3D model composition
│  │     └─ Macbook-16.jsx      # 16" model variant
│  ├─ store/index.js            # Zustand store
│  ├─ App.jsx                   # Page composition + GSAP registration
│  └─ ... other utils/constants
├─ index.html                    # App mount and meta
├─ vite.config.js                # Vite config
├─ eslint.config.js              # ESLint config
└─ package.json
```

> Tip: See `src/components/Performance.jsx` for an example of ScrollTrigger usage and mobile-optimized early returns.

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ (LTS recommended)
- pnpm, npm, or yarn (examples below use npm)

### Install
```
npm install
```

### Run in Development
```
npm run dev
```
- Starts Vite dev server (HMR enabled).
- Open the printed local URL in your browser.

### Build for Production
```
npm run build
```
- Outputs a production build to `dist/`.

### Preview Production Build
```
npm run preview
```
- Serves the built `dist/` locally for final checks.

## 🧩 Environment & Assets
- This project does not require environment variables by default.
- Place any additional static assets in `public/` and reference them by `/asset.ext`.

## 📐 Styling
- Tailwind v4 is enabled via `@tailwindcss/vite`.
- Add or edit styles in component `className` strings.
- If you introduce global CSS, follow the existing Vite + Tailwind integration.

## 🎮 3D & Animation Notes
- 3D is powered by `@react-three/fiber` (a React renderer for Three.js).
- Use `@react-three/drei` for common helpers (controls, loaders, etc.).
- GSAP `ScrollTrigger` is registered in `src/App.jsx` and used in sections like `Performance.jsx`.
- Mobile devices may reduce or skip heavy animations for performance (see `react-responsive` usage).

## 🧪 Linting
```
npm run lint
```
- ESLint is configured for React with recommended rules.

## 🛠️ Troubleshooting
- Blank canvas or model not visible:
  - Check that WebGL is available in your browser.
  - Verify model/component imports in `components/models/`.
- Scroll animations not triggering:
  - Ensure `ScrollTrigger` is registered and elements exist in DOM.
- CSS not applying:
  - Confirm Tailwind plugin is active and the dev server restarted after config changes.

## 📦 Scripts
- `dev` — start HMR dev server
- `build` — create production build
- `preview` — preview `dist/`
- `lint` — run ESLint

## 🔒 License
This project is provided as-is. If you plan to open source it, replace this section with your chosen license (e.g., MIT) and include `LICENSE` in the repository.

## 🙌 Acknowledgements
- Apple’s product pages for design inspiration
- The Three.js, R3F, GSAP, and Tailwind communities

## 📣 Contributing
PRs and issues are welcome. Please keep changes focused and include a short description and screenshots or screen recordings of UI updates.
