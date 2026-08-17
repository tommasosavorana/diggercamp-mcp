# diggercamp MCP server

Find independent music by how it sounds. Paste any Bandcamp, YouTube or SoundCloud
link and get the closest sonic matches from 4M+ independent tracks, matched by rhythm,
timbre, key and energy rather than genre tags.

This is the official remote MCP server for [diggercamp](https://diggercamp.com), the
AI music discovery platform for diggers, DJs and collectors.

## Connect

No installation needed: it is a remote server.

- **Server URL:** `https://mcp.diggercamp.com/mcp` (streamable HTTP)
- **Auth:** OAuth 2.1 with your diggercamp account (also works in guest tier without login)
- **Registry:** published as `com.diggercamp/music-similarity` on the
  [official MCP registry](https://registry.modelcontextprotocol.io)

In Claude: Settings, Connectors, Add custom connector, paste the server URL.
In ChatGPT: Settings, Connectors, Developer mode, add MCP server.
Any other MCP client that supports remote streamable HTTP servers works the same way.

## Tools

| Tool | What it does |
|---|---|
| `find_similar(url)` | Sonically similar tracks for a Bandcamp, YouTube or SoundCloud link |
| `deep_match(url)` | Technical match by rhythm, timbre and key, built for DJ sets (Pro/Studio) |
| `surprise_me(url)` | Similar tracks with more variety and less obvious picks (Pro/Studio) |
| `playlist_match(urls)` | Tracks that fit the combined sound of a set of 2 to 8 links |
| `inspire_me()` | A starting point from the diggercamp crate plus its closest matches |
| `generate_playlist(url, n, end_url, vibe)` | Generates and saves a playlist in your account (login required) |

Every result includes BPM and Camelot key for harmonic mixing, plus a direct link to
the source platform, so listening and buying always happen where the artist publishes.

## How it works

diggercamp analyses the sound itself. Every track is converted into acoustic
fingerprints that describe rhythm, timbre, energy and overall sonic character, and
similarity search runs on those fingerprints. diggercamp does not host, sell or
distribute audio files: playback happens through the source platforms, and purchase
links point to the artist's own page.

## Links

- Website: [diggercamp.com](https://diggercamp.com)
- Manifesto: [diggercamp.com/manifesto](https://diggercamp.com/manifesto)
- FAQ: [diggercamp.com/faq](https://diggercamp.com/faq)
- Contact: info@diggercamp.com

The platform code is not part of this repository; this repo documents the public MCP
endpoint and its metadata.
