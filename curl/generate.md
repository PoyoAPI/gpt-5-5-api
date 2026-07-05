# GPT-5.5 API cURL Quickstart

Use this from a backend environment. Keep `POYO_API_KEY` out of browser code.

```bash
export POYO_API_KEY="YOUR_POYO_API_KEY_HERE"

curl https://api.poyo.ai/v1/chat/completions \
  -H "Authorization: Bearer $POYO_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "model": "gpt-5.5",
  "messages": [
    {
      "role": "system",
      "content": "You are a concise senior engineering assistant."
    },
    {
      "role": "user",
      "content": "Give me a concise plan for evaluating a high-capability AI model before adding it to a production coding assistant."
    }
  ],
  "max_tokens": 600
}'
```

## Notes

- Replace `YOUR_POYO_API_KEY_HERE` with a server-side environment variable in production.
- Start with `gpt-5.5`, then route to other variants only when the workflow needs them.
- Log latency and usage so model routing decisions are based on real product behavior.

Model page: https://poyo.ai/models/gpt-5-5
