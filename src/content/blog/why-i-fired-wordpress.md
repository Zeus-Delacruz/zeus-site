---
title: "Why I Fired WordPress and Went Static"
description: "WordPress broke every time we touched it. Astro + Cloudflare Pages deploys in 30 seconds and never breaks. The full migration story."
pubDate: 2026-09-27
tags: ["build-in-public", "infrastructure", "astro"]
---

WordPress gave us 25 pages and then took them away — one `sed` command at a time.

This site ran on WordPress for exactly one week. In that week: a template edit broke every page at once, a content push hit the wrong page IDs, the cache lied about what was deployed, and every single change required SSH + WP-CLI + cache flush + prayer.

## The breaking point

The final straw was a nav update. One link. To add it we had to:

1. SSH into the droplet
2. `sed` a PHP template file
3. Hope no quote characters broke
4. Flush the cache
5. Verify by curl
6. Repeat when it broke anyway

That's not a workflow. That's archaeology.

## The stack now

```
GitHub repo (Zeus-Delacruz/zeus-site)
  → git push to main
  → Cloudflare Pages auto-builds (npm run build)
  → static HTML on a global CDN
  → live in ~30 seconds
```

No database. No PHP. No cache flush. No SSH. The site you're reading this on is a set of static files served from 300+ edge locations, for free.

## What we lost

Nothing. Forms still work (Zoho embeds are just `<script>` tags). The blog is markdown files — easier than the WP editor. The design system is one CSS file.

## What we gained

- **Deploys in 30 seconds**, not 5 minutes of tool wrestling
- **Every change is a git commit** — full history, full rollback
- **Zero breaking changes possible** — static files can't fight each other
- **Free hosting** — the $6/mo droplet is now powered off
- **Instant cache purge** — every deploy is a fresh cache, automatically

The WordPress droplet still exists, powered off, as a snapshot of the old world. It won't be missed.
