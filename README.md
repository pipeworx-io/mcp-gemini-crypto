# @pipeworx/gemini-crypto

[Gemini Exchange](https://docs.gemini.com/rest-api/) MCP — keyless public market endpoints.

Part of [Pipeworx](https://pipeworx.io) — an MCP gateway connecting AI agents to 1394+ live data sources.

## Tools

- `symbols()` — list trading pairs
- `symbol_details(symbol)` — pair metadata
- `ticker(symbol)` — v1 ticker
- `ticker_v2(symbol)` — v2 ticker (24h stats)
- `candles(symbol, time_frame)` — candles (`1m|5m|15m|30m|1hr|6hr|1day`)
- `book(symbol, limit_bids?, limit_asks?)` — orderbook
- `trades(symbol, timestamp?, limit_trades?, include_breaks?)` — trade history
- `price_feed()` — price feed (all symbols)
- `network(token)` — network for a token (e.g. `btc`)
- `gas_fees(symbol)` — gas fee estimate

## Data source

`https://api.gemini.com`

## Quick Start

Add to your MCP client (Claude Desktop, Cursor, Windsurf, etc.):

```json
{
  "mcpServers": {
    "gemini-crypto": {
      "url": "https://gateway.pipeworx.io/gemini-crypto/mcp"
    }
  }
}
```

Or connect to the full Pipeworx gateway for access to all 1394+ data sources:

```json
{
  "mcpServers": {
    "pipeworx": {
      "url": "https://gateway.pipeworx.io/mcp"
    }
  }
}
```

## Using with ask_pipeworx

Instead of calling tools directly, you can ask questions in plain English:

```
ask_pipeworx({ question: "your question about Gemini Crypto data" })
```

The gateway picks the right tool and fills the arguments automatically.

## More

- [Docs and guides](https://pipeworx.io/docs)
- [pipeworx.io](https://pipeworx.io)

## License

MIT
