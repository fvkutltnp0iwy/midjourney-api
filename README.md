# Midjourney API (midjourney) — api guide with published pricing

> **default $0.045; imagine $0.045; imagine-niji6 $0.045** — flat per-unit billing through the OpenAI-compatible APIMart gateway, $1 minimum top-up.

**[Live pricing](https://apimart.ai/pricing)** · **[Get an API key](https://apimart.ai/keys)**

Everything here refers to **midjourney** — also written **midjourney** or **midjourney**.

## Pricing (observed, snapshot 2026-09-24)

| Tier | Price |
| --- | --- |
| `default` | $0.045 |
| `imagine` | $0.045 |
| `imagine-niji6` | $0.045 |
| `imagine-niji7` | $0.045 |

## Cost at scale

| Volume | Cost |
| --- | --- |
| 100 | $4.504 |
| 1,000 | $45.04 |

## How to call it

```bash
curl --request POST --url https://api.apimart.ai/v1/images/generations \
  --header "Authorization: Bearer $APIMART_API_KEY" --header 'Content-Type: application/json' \
  --data '{"model":"midjourney","prompt":"a modern cliffside villa at dusk","size":"16:9","n":1}'
```

Submit, keep the `task_id`, poll `GET /v1/tasks/{id}` until `completed`; the response carries the URL and the exact amount charged.

## Disclosure

Documents access through APIMart, a third-party API gateway; not affiliated with the model vendor.
