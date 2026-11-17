# Polymarket

Query Polymarket prediction-market data — markets, prices, orderbooks, history — through public REST APIs. Read-only, zero authentication.

## What it is

An agent skill (v1.0.0) for reading Polymarket: what are the odds of X happening, and how are they moving?

**Prices are probabilities:** a price of 0.65 means the market thinks the event is 65% likely. Volume is in USDC.

## Three public APIs

1. **Gamma API** (`gamma-api.polymarket.com`) — discovery, search, browsing
2. **CLOB API** (`clob.polymarket.com`) — real-time prices, orderbooks, history
3. **Data API** (`data-api.polymarket.com`) — trades, open interest

## What's inside

- `SKILL.md` — the skill definition, concepts, and workflow
- `references/api-endpoints.md` — the full endpoint reference with curl examples

## Quick start

Search for a market, parse the response, present prices as percentages:

```
"Will X happen?" — 65.2% Yes ($1.2M volume)
```

Deep dive with `clobTokenIds` (orderbook) and `conditionId` (price history).

## Limitations

- **Read-only.** This skill does not place trades. Trading needs wallet-based crypto authentication (EIP-712 signatures).
- Some new markets may have empty price history.
- Geographic restrictions apply to trading; read-only data is globally accessible.

## License

MIT — see [LICENSE](LICENSE).
