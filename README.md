# Gemini 3 Pro API (gemini-3-pro / gemini3pro) — llm-pricing guide with published pricing

> **input $1.6; output $9.6** — flat per-unit billing through the OpenAI-compatible APIMart gateway, $1 minimum top-up.

**[Live pricing](https://apimart.ai/pricing)** · **[Get an API key](https://apimart.ai/keys)**

Everything here refers to **gemini-3-pro** — also written **gemini3pro** or **gemini 3 pro**.

## Pricing (observed, snapshot 2026-09-24)

| Tier | Price |
| --- | --- |
| `input` | $1.6 |
| `output` | $9.6 |

## Cost at scale

| Volume | Cost |
| --- | --- |
| 100 | $160 |
| 1,000 | $1,600 |

## How to call it

```bash
curl --request POST --url https://api.apimart.ai/v1/images/generations \
  --header "Authorization: Bearer $APIMART_API_KEY" --header 'Content-Type: application/json' \
  --data '{"model":"gemini-3-pro-preview","prompt":"a modern cliffside villa at dusk","size":"16:9","n":1}'
```

Submit, keep the `task_id`, poll `GET /v1/tasks/{id}` until `completed`; the response carries the URL and the exact amount charged.

## Disclosure

Documents access through APIMart, a third-party API gateway; not affiliated with the model vendor.
