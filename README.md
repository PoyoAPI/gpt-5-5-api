# GPT-5.5 API Examples for PoYo

[![Model page](https://img.shields.io/badge/Model%20page-gpt--5--5-84cc16)](https://poyo.ai/models/gpt-5-5)
[![API docs](https://img.shields.io/badge/API%20docs-docs.poyo.ai-22d3ee)](https://docs.poyo.ai/api-manual/chat-series/chat-completions)
[![License: MIT](https://img.shields.io/badge/License-MIT-111827)](LICENSE)
[![Main examples](https://img.shields.io/badge/Main%20examples-PoyoAPI%2Fpoyo--examples-0f172a?logo=github)](https://github.com/PoyoAPI/poyo-examples)

Focused server-side examples for building GPT-5.5 chat, coding, and agent workflows on PoYo.

GPT-5.5 is useful for high-accuracy knowledge work, coding assistants, planning agents, and production chat workflows that need a strong general model path.

[Model Page](https://poyo.ai/models/gpt-5-5) | [Docs](https://docs.poyo.ai/api-manual/chat-series/chat-completions) | [Get API Key](https://poyo.ai/dashboard/api-key) | [Pricing](https://poyo.ai/pricing) | [Main Examples](https://github.com/PoyoAPI/poyo-examples)

## What This Repo Covers

- Chat completions with `gpt-5.5`
- OpenAI-style `/v1/chat/completions` requests
- Server-side API key handling
- Node.js backend example
- Prompt examples and production integration notes

## Quick Start

```bash
cp .env.example .env
export POYO_API_KEY="your-api-key"
```

Run the Node.js example:

```bash
cd node
npm start
```

Keep `POYO_API_KEY` on the server. Do not expose it in browser code, mobile apps, screenshots, or public logs.

## Production Pattern

- Keep `POYO_API_KEY` on the server
- Send a chat completion request
- Log model, latency, and usage for cost tracking
- Add retries around network failures, not around every model response

## Models

This repo uses `gpt-5.5`.

## Examples

| Path | What it covers |
| --- | --- |
| [`curl/generate.md`](curl/generate.md) | Copy-paste API request. |
| [`node/`](node/) | Native Node.js backend example. |
| [`docs/prompt-examples.md`](docs/prompt-examples.md) | Practical prompts for product workflows and creative tests. |
| [`docs/production-notes.md`](docs/production-notes.md) | Security and reliability notes before launch. |

## Run Checks

```bash
make check
```

On Windows:

```powershell
./scripts/check.ps1
```

## License

MIT
