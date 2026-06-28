# Gusty

Personal portfolio for Güney Usta: design, writing, and AI-assisted systems.

- Live: [gusty.ch](https://gusty.ch)
- Stack: Next.js 16, React 19, TypeScript, Tailwind CSS
- Deploy: Vercel

## What It Does

- Shows portfolio projects across human-made, AI-assisted, and teamed-up work
- Supports English and German copy
- Opens rich project notes in modals
- Keeps experimental work behind an env-gated danger zone

## Project Content

- Project data lives in `lib/projects/`
- `lib/projects/index.ts` controls what appears on gusty.ch
- Each project exports one `Project` object
- Set `column` to `design`, `ai`, `bridged`, or `danger`

## Run Locally

```bash
npm install
npm run dev
npm run build
```

## Main Files

- `app/page.tsx`: homepage grid
- `components/ProjectCard.tsx`: project cards
- `components/ProjectModal.tsx`: project detail modal
- `lib/i18n/`: language state and UI strings
- `lib/projects/`: portfolio content

## License

Private. All rights reserved.
