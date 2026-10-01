# AGENTS.md

## What this repo is

**`docs`** — customer-facing help centre for REalyse Core, REalyse MCP, and REalyse Pulse, built with Mintlify. Pushes to `main` deploy to production through the Mintlify GitHub app.

## Company standards

Shared engineering rules live in `realyse/standards`, not this repo. **This file wins** for this repository's folders, commands, and project-specific behaviour.

Locate a checkout, in order:

1. A workspace folder named `standards`.
2. Sibling `../standards`, or `../core/standards` when this clone sits under `core/`.
3. `./.realyse-standards` (gitignored; do not commit it).

If none exist:

```bash
git clone git@github.com:realyse/standards.git .realyse-standards
```

Then read that checkout's `AGENTS.md` and `docs/contributing/git-and-reviews.md`. Do not treat a GitHub URL as already-loaded rules.

## Where to change things

| Task | Location |
|---|---|
| Help pages | `core/`, `mcp/`, `pulse/` (`.mdx` with `title` and `description`) |
| Navigation and site config | `docs.json` |
| Home page | `index.mdx` |
| Brand assets | `logo/`, `favicon.svg` |
| Drafts (unpublished) | `drafts/` or `*.draft.mdx` |

A new page appears on the site only after its path, without the extension, is listed in `docs.json`. `.mintignore` keeps `drafts/` and `*.draft.mdx` out of the published site.

## How to run it

Install the Mintlify CLI if needed (`npm i -g mint`), then from this repository root:

```bash
mint dev
```

The preview runs at `http://localhost:3000`. If it does not start, run `mint update`. If a page returns 404, confirm you are in the folder that contains `docs.json` and that the page is listed in its navigation.

For Mintlify component and configuration reference, install the Mintlify skill: `npx skills add https://mintlify.com/docs`.

**Branch:** `main`.

## Style

Write for customers. Use active voice and second person ("you"). Keep sentences to one idea. Use sentence case for headings. Bold UI labels, as in Click **Settings**. Use code formatting for file names, commands, paths, and code references.

Product names are REalyse Core, REalyse MCP, and REalyse Pulse. Use British spelling, as in "help centre".

This site covers customer help for those three products. Internal engineering rules stay in `realyse/standards`. Customer questions go to support@realyse.com.
