# REalyse help centre

Customer-facing help and guides for REalyse products, built with [Mintlify](https://mintlify.com). Pushes to `main` deploy to production automatically through the Mintlify GitHub app.

## What's in here

The site is split into three products, each with its own tab in the navigation.

| Folder | Product | Covers |
|---|---|---|
| `core/` | REalyse Core | Projects, data and locations, exports, account |
| `mcp/` | REalyse MCP | Connecting AI assistants, authentication, tools, data coverage, usage limits, troubleshooting |
| `pulse/` | REalyse Pulse | Property valuations, reports, account and billing |

Other files:

- `index.mdx` is the help centre home page.
- `docs.json` holds site configuration and navigation. A new page only appears on the site once it's listed here.
- `logo/` and `favicon.svg` are brand assets.
- `AGENTS.md` has writing and style instructions for AI tools.

## Run it locally

Install the Mintlify CLI:

```bash
npm i -g mint
```

From the repository root, where `docs.json` lives, run:

```bash
mint dev
```

The preview runs at `http://localhost:3000`. If it doesn't start, run `mint update` to get the latest CLI. If a page returns 404, check that you're running from the folder that contains `docs.json` and that the page is listed in its navigation.

## Adding or changing pages

1. Write the page as an `.mdx` file with YAML frontmatter (`title` and `description` at minimum) in the right product folder.
2. Add the page path, without the extension, to the right group in `docs.json`.
3. Preview it with `mint dev`, then open a pull request against `main`.

Put work in progress under `drafts/` or name it `*.draft.mdx`. `.mintignore` keeps both out of the published site.

Follow the style rules in `AGENTS.md`: use active voice, address the reader as "you", use sentence case for headings, and bold UI labels.

## AI-assisted writing

To give your AI coding tool Mintlify's component reference and writing guidance, run:

```bash
npx skills add https://mintlify.com/docs
```

## Support

Customer questions go to [support@realyse.com](mailto:support@realyse.com).
