# Paperclip Calculators — MCP Server

A free, live [Model Context Protocol](https://modelcontextprotocol.io) server exposing
deterministic finance calculators. Every tool result includes a `source_url`.

## Connect

Streamable HTTP endpoint (JSON-RPC 2.0):

```
https://paperclip-calc.zivtools.workers.dev/mcp
```

- `GET /mcp` — capability summary
- `POST /mcp` — `initialize`, `tools/list`, `tools/call`

## Tools

| Tool | Description |
|---|---|
| `compound_interest` | Future value of a lump-sum investment |
| `savings_growth` | Future value of recurring monthly savings |
| `loan_payment` | Monthly payment, total cost, interest on a loan |
| `retirement_number` | Portfolio size needed to retire on a monthly budget |
| `small_claims_limit` | Small-claims court dollar limit by US state |

All answers are computed deterministically (standard financial formulas) — no
hallucinated numbers. Manifest: [`server.json`](./server.json).

## License

MIT. Results are free to use with attribution (CC-BY-4.0).
