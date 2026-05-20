---
name: awesome-design-md
description: "Select and apply a fitting Awesome Design MD `DESIGN.md` style for frontend/UI work. Use when the user asks to design UI, redesign a page, beautify a frontend, create a dashboard, improve layout/visual hierarchy, change visual style, use a big-company design style, or mentions `DESIGN.md`, Awesome Design MD, big-tech styles, brand-inspired UI, Apple/Stripe/Linear/Cursor/Raycast/Voltagent/Binance/Coinbase/xAI-style interfaces."
---

# Awesome Design MD

## Purpose

Use the bundled Awesome Design MD library as a selectable reference set for UI design. Do not assume one global style. Pick the style that best fits the product, then read that style's `DESIGN.md` before changing UI.

Resolve all library paths relative to this skill folder, meaning the directory that contains this `SKILL.md`.

Bundled library:

`<skill-root>/design-md`

Style index:

`<skill-root>/STYLE_INDEX.txt`

Style file pattern:

`<skill-root>/design-md/<style>/DESIGN.md`

Optional selection notes:

`<skill-root>/references/style-selection.md`

## Workflow

1. If the user names a style, use that exact style when it exists.
2. If no style is named, inspect the product context and choose 1 style. Mention the chosen style briefly before editing.
3. Read `STYLE_INDEX.txt` if you need to see available styles.
4. Read only the selected `design-md/<style>/DESIGN.md`; do not load the whole library.
5. Apply the style as guidance for layout, color, typography, spacing, interaction feel, and component chrome.
6. Preserve existing product constraints, data density, accessibility, and framework conventions.
7. For existing apps, evolve the UI without breaking established flows unless the user explicitly asks for a redesign.

## Default Style Mapping

- Developer tool, AI agent console, automation panel: `voltagent`, `cursor`, `warp`, `linear.app`, `raycast`.
- SaaS dashboard, task/project management, admin console: `linear.app`, `stripe`, `vercel`, `posthog`, `supabase`.
- Consumer/mobile-like polished product: `apple`, `airbnb`, `spotify`, `pinterest`, `notion`.
- Crypto/Web3/exchange/finance: `coinbase`, `binance`, `kraken`, `revolut`, `wise`.
- AI lab/model/product page: `x.ai`, `mistral.ai`, `cohere`, `together.ai`, `runwayml`, `replicate`.
- Docs/developer portal: `mintlify`, `vercel`, `stripe`, `supabase`, `hashicorp`.
- Luxury/automotive/brand-heavy landing page: `bugatti`, `ferrari`, `lamborghini`, `bmw`, `tesla`, `nike`.

If several styles fit, choose the one that improves the specific screen most, not the flashiest one.

## Rules

- Do not blindly apply `voltagent` everywhere.
- Do not import a `DESIGN.md` into the target project unless the user asks; reading from the bundled library is enough.
- Do not copy large chunks of design text into the final answer.
- Do not override a project-level `DESIGN.md`; if it exists, treat it as the local routing note and then read the selected bundled style.
- Avoid generic AI UI defaults. Use the selected style's concrete tokens and component habits.
- For projects that require a specific file encoding, follow the project's local instruction.

## Quick Commands

List available styles from the skill root:

```powershell
Get-Content -LiteralPath '.\STYLE_INDEX.txt'
```

Read one style from the skill root:

```powershell
Get-Content -Raw -Encoding UTF8 -LiteralPath '.\design-md\linear.app\DESIGN.md'
```
