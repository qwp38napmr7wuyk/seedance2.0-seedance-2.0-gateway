# Seedance 2.0 API (seedance-2.0 / seedance2.0) — gateway guide with published pricing

> **480P-input $0.04; 480P $0.066; 720P-input $0.0858** — flat per-unit billing through the OpenAI-compatible APIMart gateway, $1 minimum top-up.

**[Live pricing](https://go.apimart.ai/k-b77bd2)** · **[Get an API key](https://go.apimart.ai/k-f16743)**

Everything here refers to **seedance-2.0** — also written **seedance2.0** or **seedance 2.0**.

## Pricing (observed, snapshot 2026-09-24)

| Tier | Price |
| --- | --- |
| `480P-input` | $0.04 |
| `480P` | $0.066 |
| `720P-input` | $0.0858 |
| `720P` | $0.142 |

## Cost at scale

| Volume | Cost |
| --- | --- |
| 100 | $4 |
| 1,000 | $40 |

## How to call it

```bash
curl --request POST --url https://api.apimart.ai/v1/videos/generations \
  --header "Authorization: Bearer $APIMART_API_KEY" --header 'Content-Type: application/json' \
  --data '{"model":"seedance-2.0","prompt":"a modern cliffside villa at dusk","size":"16:9","n":1}'
```

Submit, keep the `task_id`, poll `GET /v1/tasks/{id}` until `completed`; the response carries the URL and the exact amount charged.

## Disclosure

Documents access through APIMart, a third-party API gateway; not affiliated with the model vendor.
