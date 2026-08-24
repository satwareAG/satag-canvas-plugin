# satware® AI Canvas

TypingMind plugin that lets the AI render **interactive HTML canvases** in the chat: forms, HTML/JS/CSS apps, games, visualizations, charts, and any other interactive content. Runs natively in the browser iframe - no server process, no MCP dependency.

## Tools

- **`render_interactive_canvas`**: Render a complete HTML document as an interactive canvas. Use for the first render and full rewrites.
- **`update_interactive_canvas`**: Apply small find-and-replace edits to the most recently rendered canvas. Much faster and uses far fewer tokens than re-emitting the whole HTML.

## Environment constraints (enforced by the sandbox)

1. The rendering iframe has no `allow-same-origin`: `localStorage`, `sessionStorage`, `indexedDB`, and `document.cookie` throw `SecurityError`. Use plain in-memory state.
2. Strict CSP: external scripts load only from whitelisted CDNs (`cdn.jsdelivr.net`, `cdnjs.cloudflare.com`, `ajax.googleapis.com`, `ajax.aspnetcdn.com`, `unpkg.com`, `stackpath.bootstrapcdn.com`). Notably `cdn.tailwindcss.com` is blocked - use the cdnjs CSS variant.
3. Deferred asset pipeline: render a lightweight loading screen first, inject external dependencies asynchronously, then launch the app view.

## Installation

Import `plugin.json` on your TypingMind instance (Plugins > Import). The primary function loads `implementation.js` from this repository.

## License

MIT - see [LICENSE](LICENSE).
