# FeatPaper for Claude

FeatPaper turns a PDF into a share link and shows who read which page. This plugin connects Claude to FeatPaper: it adds the `featpaper` skill and the FeatPaper connector (`https://mcp.featpaper.com/mcp`).

## What it does

- **Make a document.** Claude shows the PC (16:9) version in an editable format first. Desktop and mobile PDFs are made when you ask to publish.
- **Publish and share.** After you sign in to FeatPaper, Claude uploads the PDF and its source text, registers the document and returns the share link. It can also make per-recipient links and links that ask for contact details first.
- **Read a FeatPaper link.** Claude reads a feat.page or featpaper.com document you were sent, with page numbers, without signing in.
- **See who read it.** For your own documents, Claude reports who opened them, when, and how long they spent on each page.

Claude uses the skill only when you mention feat or FeatPaper or ask for a FeatPaper link or upload.

## Install

In Claude Code:

```
/plugin marketplace add org-feat/featpaper-claude-plugin
/plugin install featpaper@featpaper
```

In claude.ai and Claude desktop, add FeatPaper from the Connectors directory.

## Data and privacy

- Creating documents and reading public FeatPaper links work without an account. Registering, sharing and statistics need a FeatPaper account and happen only when you ask.
- Registering uploads your PDFs, the source text and the optional mobile summary page to your FeatPaper account. Nothing is shared publicly unless you choose a public setting.
- The plugin stores no credentials and makes no network request of its own; all requests go through the connector.
- `plugin/skills/featpaper/references/mobile-summary-kit.html` is a preview script that Claude pastes into a mobile summary page it writes. It runs only inside that page and sends `ready`, `section`, `activity` and `cta` messages to the FeatPaper viewer that embeds the page.

Privacy policy: https://featpaper.com/en/privacy/ · Terms: https://featpaper.com/en/terms/

## Support

Documentation: https://featpaper.com/docs/ · Email: hello@wefeat.kr

## License

MIT (see `LICENSE`).
