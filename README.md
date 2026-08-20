# roadmap.kurult.ai

Canonical Parse + Hulegu launch roadmaps for [Kurultai](https://kurult.ai). Ghazan owns the copy. x402 OFF. No certifications. Scoring weights unpublished. No secrets.

## Invariants

- No build system, no framework, no webfonts, no analytics. The committed files are the artifact.
- Ghazan owns product truth. Front end hosts what he stamps; empty or unknown stays empty or unknown.
- No books, no personal mail, no secrets, API tokens, agent UUIDs, or `.env` in this repo.
- Nobody sends email or LinkedIn from this host.
- Do not invent Cloudflare Access in the HTML. Access is Kublai's wrap, not a minted key on this page.
- One roadmap repo and one Pages project (`roadmap-kurult-ai`). Do not invent a second project.
- `llms.txt` lists this public host and durable public surfaces only — never gated hostnames.

## Deploy

Cloudflare Pages, direct upload of the repo root:

```sh
CLOUDFLARE_API_TOKEN=$(cat ~/.kublai/secrets/cloudflare-pages-api-token) \
  npx wrangler@latest pages deploy . --project-name roadmap-kurult-ai
```

Break-glass (no CLI): Cloudflare dashboard → Workers & Pages → roadmap-kurult-ai → Create deployment → drag this folder in.

Custom domain: attach `roadmap.kurult.ai` in Pages → Custom domains. Do not touch `kurult.ai` MX / mail records.

Public Pages auto-deploy after merge to `main`. Merge, Access wrap, and domain attach wait on Danny / Kublai.

Rollback: redeploy any prior deployment from the Pages dashboard (one click).

## Verify after deploy

```sh
curl -sI https://roadmap.kurult.ai/            # 200 text/html, server: cloudflare
curl -sI https://roadmap.kurult.ai/llms.txt    # 200 text/plain
dig +short kurult.ai MX                        # unchanged — mail records are never touched
```
