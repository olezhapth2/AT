# AT Project — Agent Guide

## Project Overview
Landing page for AT.ai franchise — AI-powered leasing business system.
Target audience: ROPs, directors in leasing/banking/insurance.

## Repo
- GitHub: `https://github.com/olezhapth2/AT.git`
- Branch: `main`
- GitHub Pages: `https://olezhapth2.github.io/AT/at-landing/`
- Deploy: push to `main` → auto-builds on GitHub Pages

## Structure
```
attecno/
├── at-landing/          ← main work directory
│   ├── index.html       ← single-file landing (HTML + CSS + JS, ~3300 lines)
│   ├── call.mp3         ← audio for case section
│   └── bg-[1-20].jpg    ← B&W background illustrations
├── vesper/              ← reference site (Vesper.ai)
└── AGENTS.md            ← this file
```

## Design System
- **Palette**: 3 colors only — `#000000` (bg), `#ffffff` (text), `#9a9a9a` (muted)
- **Fonts**: Inter (UI) + Instrument Serif italic (emphasis in headings only)
- **CSS vars**: `--bg`, `--text`, `--muted`, `--border`, `--glass`, `--glass-border`, `--card-bg`, `--content-max`, `--section-gap`
- **Style**: Vesper.ai liquid-metal glass aesthetic — dark, minimal, glassmorphism

## Conventions
- All code in single `index.html` (inline `<style>` + `<script>`)
- No build tools, no frameworks — vanilla HTML/CSS/JS
- Section labels (надзаголовки) are removed — user says they look AI-generated
- No "Подробнее" buttons on bento cards
- Bento grid: Apple-style cards with unique animations per card
- Animations: CSS keyframes + requestAnimationFrame for scroll effects
- Scroll focus ring: blurs content at top 15% and bottom 25% of viewport (disabled for bento on mobile)
- Form: Formspree (`xqpaazan`) → sends to `artyom.tonnikov@gmail.com`

## Key Sections (in order)
1. Hero — headline + CTA buttons
2. About — what AT is
3. Case — audio player + results
4. How — step-by-step process
5. Scale — bento grid with 6 advantage cards
6. Economics — 24-month timeline
7. Trust — partner logos + trust finale
8. CTA — application form

## Removed Sections (do NOT re-add)
- "Почему руководители уходят из бизнеса" (problem section)
- "Минусы франшизы" block
- Footer
- Font switcher
- Typography settings panel
- Case-final block (72,090 ₽)

## Mobile
- Breakpoint: 900px (tablet), 768px (mobile)
- Header: always visible with CTA button + burger menu
- Bento grid: 1-col on mobile, no scroll blur effect
- Hero: `padding-bottom: 100px`

## Deployment
```bash
git add . && git commit -m "description" && git push
# GitHub Pages auto-builds from main branch
```

## Figma
- Figma MCP bridge available but largely abandoned (poor quality translation)
- Figma node `311:1436` — "AT Landing" frame (partial)
