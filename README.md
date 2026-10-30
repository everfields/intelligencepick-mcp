# Intelligence Pick

AI picks for every product category: the product an AI model would buy, why, and who should skip it.

This repository is the public listing for the **Intelligence Pick** remote MCP server. It holds no code; the server is hosted.

## Endpoint

- URL: `https://intelligencepick.com/mcp`
- Transport: streamable HTTP
- Auth: `X-API-Key` header. Get a free key at https://intelligencepick.com/developers

## Tools

- `get_pick`: the product an AI model would buy in a product category, with why and who should not buy it. Accepts a category name or query, an id or an intelligencepick.com URL.
- `search_categories`: find product categories covered by Intelligence Pick. Returns up to 10 names with their URLs.
- `get_brief_summary`: the pick, picks by need, the criteria that matter and the brands that count for one category, with provenance and the source URL.

## Client config

```json
{
  "mcpServers": {
    "intelligence-pick": {
      "type": "streamable-http",
      "url": "https://intelligencepick.com/mcp",
      "headers": { "X-API-Key": "<your key>" }
    }
  }
}
```

## Links

- Developers: https://intelligencepick.com/developers
- Server card: https://intelligencepick.com/.well-known/mcp/server-card.json
- Official MCP registry id: `com.intelligencepick/picks` (version 1.0.0)
- Glama: https://glama.ai/mcp/connectors/com.intelligencepick/picks
