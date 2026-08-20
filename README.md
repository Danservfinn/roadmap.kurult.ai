# roadmap.kurult.ai

Canonical Parse + Hulegu launch roadmaps for [Kurultai](https://kurult.ai). Ghazan owns the copy. x402 OFF. No certifications. Scoring weights unpublished. No secrets.

## Invariants

- No build system, no framework, no webfonts, no analytics. The committed files are the artifact.
- Ghazan owns product truth. Product claims from live parsethis.ai only. Dated lab snapshots are unknown as standing truth.
- No books, no personal mail, no secrets, API tokens, agent UUIDs, or `.env` in this repo.
- Nobody sends email or LinkedIn from this host.
- Do not invent Cloudflare Access in the HTML. Access is Kublai's wrap, not a minted key on this page.
- One roadmap repo only: `Danservfinn/roadmap.kurult.ai`. Do not invent a second repo.
- Origin is the Mini, same class as `life.kurult.ai` — not Cloudflare Pages as the host. `wrangler.toml` may remain as a leftover file; it is not how this host is served.
- `llms.txt` lists the intended hostname and durable public surfaces only — never gated hostnames, never a live-host claim while NXDOMAIN.

## Host

Mini origin (Danny lock), same class as `life.kurult.ai`. Kublai points the hostname `roadmap.kurult.ai`. Do not invent DNS. Do not touch `kurult.ai` MX / mail records.

Access is Kublai's wrap after the hostname is pointed — not a minted key in this HTML, and not described here as live until that wrap exists.

Merge waits on Orda receipt + approve-deploy. This PR stays draft until then.

## Source

Static files in this repo are the board copy. They are not served by Cloudflare Pages auto-deploy, `wrangler pages deploy`, or a Pages custom-domain attach. Those paths are not the host story for this site.

## Verify after host is pointed (Kublai)

```sh
dig +short kurult.ai MX                        # unchanged — mail records are never touched
```

Do not treat a Pages URL or a `*.pages.dev` hostname as this origin. Do not post a live roadmap URL until Kublai has pointed the hostname and Orda has receipted.
