# AgentsDock website

Static product and download site for AgentsDock.

## Preview

```bash
cd website
npm run dev
```

Open `http://localhost:4175`.

## Publish a desktop release

1. Publish signed artifacts through the public release repository and use their immutable versioned URLs in `website/releases/latest.json`.
2. Add each artifact's SHA256 to `website/releases/latest.json`.
3. Set the platform's `available` value to `true`.
4. Deploy the contents of `website/` to any static host.

The UI reads `releases/latest.json` at runtime, so releases do not require rebuilding the website.
