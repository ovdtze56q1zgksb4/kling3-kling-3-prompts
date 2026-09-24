# Kling v3 API (kling-3 / kling3) — prompts guide with published pricing

> **default $0.0672; pro $0.0896; sound $0.1008** — flat per-unit billing through the OpenAI-compatible APIMart gateway, $1 minimum top-up.

**[Live pricing](https://go.apimart.ai/k-d5dc50)** · **[Get an API key](https://go.apimart.ai/k-f06f72)**

Everything here refers to **kling-3** — also written **kling3** or **kling 3**.

## Pricing (observed, snapshot 2026-09-24)

| Tier | Price |
| --- | --- |
| `default` | $0.0672 |
| `pro` | $0.0896 |
| `sound` | $0.1008 |
| `pro-sound` | $0.1344 |

## Cost at scale

| Volume | Cost |
| --- | --- |
| 100 | $6.72 |
| 1,000 | $67.2 |

## How to call it

```bash
curl --request POST --url https://api.apimart.ai/v1/videos/generations \
  --header "Authorization: Bearer $APIMART_API_KEY" --header 'Content-Type: application/json' \
  --data '{"model":"kling-v3","prompt":"a modern cliffside villa at dusk","size":"16:9","n":1}'
```

Submit, keep the `task_id`, poll `GET /v1/tasks/{id}` until `completed`; the response carries the URL and the exact amount charged.

## Disclosure

Documents access through APIMart, a third-party API gateway; not affiliated with the model vendor.
