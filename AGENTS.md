# AGENTS.md

Personal site and blog of Nimit Bhardwaj: https://nimitbhardwaj.github.io

Astro + [AstroPaper](https://github.com/satnaing/astro-paper) theme, Bun, deployed to GitHub Pages by GitHub Actions on push to `main`.

## The most important rule

**Nimit writes all content himself** (posts, About, home intro). Do not write or add content on your own.

Your job on content is only:
1. Fix spelling and grammar.
2. Check and fix technical details (commands, config, facts).
3. Suggest, and wait for approval before changing wording or structure.

Keep his voice. Simple, human, Indian English. Do not make it sound like AI: no em dashes, no hype words (passionate, delve, journey, game-changer), no corporate tone. Do not "improve" a sentence that is already clear.

## Ask first, always

- **Do not push or commit** unless asked.
- **Do not install anything** (brew, npm -g, pip, system tools) without asking.
- Do not touch his VPS, phone or other devices without asking.

## Do not publish

- Phone number, home address or other personal details.
- Tailnet IPs (100.x.x.x), `*.ts.net` names, hostnames, API keys, tokens, SSH keys.
- The Weavee project (not public yet).
- The name of the app he tests with on the phone. Keep it unnamed in public.
- The work on pulling dropdown lists from a rival app. Left out on purpose, legal risk.
- Internal employer details beyond what is already on the resume page.

## Layout

| What | Where |
|---|---|
| Posts | `src/content/posts/*.md` |
| About page | `src/content/pages/about.md` |
| Resume page | `src/content/pages/resume.md` |
| Home intro | `src/pages/index.astro` |
| Site settings, socials | `astro-paper.config.ts` |
| Favicon | `public/favicon.svg` |
| Deploy workflow | `.github/workflows/deploy.yml` |

Post front matter needs `title`, `description`, `pubDatetime`, and `tags`. Add `draft: true` to hide a post (drafts are hidden everywhere, even in dev). Images go in `src/assets/images/`, linked as `@/assets/images/name.png`.

## Commands

```bash
bun install
bun run dev      # http://localhost:4321
bun run build    # also runs astro check
```

Run `bun run build` before saying something is done.
