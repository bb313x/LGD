# CLAUDE.md — Lets Grow Digital (LGD)

## Project Overview
Marketing website for Lets Grow Digital, an AI-powered digital marketing agency for small businesses.
- **Live URL:** letsgrowdigital.ai
- **GitHub repo:** bb313x/LGD
- **Owner:** Bryan Boutins
- **Business partner:** Kirk (sales, marketing, biz dev) — "Keep It Simple" principle applies to all copy and UX

## Tech Stack
- Single-file HTML/CSS/JS — no frameworks, no build tools
- **Main file:** `lgd_website_v2.html`
- **Deployment:** GitHub → Hostinger manual deploy via hPanel
- **API proxy:** Cloudflare Worker (`lgd-monday-proxy`) for Monday.com lead capture
- **CRM:** Monday.com (workspace: bryanboutins-team)

## Design System
- Dark purple to magenta gradient color palette
- Dark theme, bold typography, high contrast
- Partner badges included in layout
- CSS variables used for all colors and design tokens

## Lead Capture
- Monday.com WorkForm embedded in site
- Form submissions proxied through `lgd-monday-proxy` Cloudflare Worker
- **API token is NEVER in client-side code** — always in Worker environment

## Deployment Workflow
1. Edit `lgd_website_v2.html` locally
2. Commit and push to GitHub
3. Deploy manually via Hostinger hPanel
4. Cloudflare Worker handles Monday.com submissions independently

## Coding Conventions
- Single-file architecture is intentional — do not split into separate CSS/JS files
- Mobile-responsive by default
- No npm, no node_modules, no build step
- Sparse comments — only where non-obvious

## What Claude Should NOT Do
- Do not suggest multi-file architecture
- Do not add npm dependencies or build tools
- Do not expose Monday.com API token in client-side code
- Do not redesign the color scheme without explicit instruction
- Do not use placeholder copy — ask if real copy is needed
