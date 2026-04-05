# 8ein Sport

**Full-stack progressive web experience** — built to feel fast, clean, and intentional. The idea is simple: bring **multimedia entertainment**, **discoverability**, and room for **knowledge and smart tooling** into one cohesive surface — not a cluttered portal, but something you actually want to open every day.

> **More than a side project — it’s a vision:** give people everything they love in **one fast, clean platform**. Built solo. Scaled independently. No excuses — just execution.

---

## At a glance

| | |
|---|---|
| **What it is** | A modern sports & streaming-oriented web app: browse sports, channels, and matches, then jump into playback with a polished video experience. |
| **How it’s built** | TypeScript end-to-end, containerized services, API-driven data — designed to grow from demo to production. |
| **Who it’s for** | Fans who want clarity — what’s on, when, and where to watch — without fighting the UI. |

---

<!-- IMAGES: Add screenshots to docs/about/ and match filenames below. -->

<p align="center">
  <img src="docs/about/hero-home.png" alt="8ein Sport — home / hero (add your screenshot)" width="720" />
</p>

<p align="center"><em>Replace <code>docs/about/hero-home.png</code> with your file — same folder for all preview images.</em></p>

---

## Key sections (product map)

### Home & discovery

Landing experience with **hero slideshow**, featured content, and quick paths into the rest of the app — tuned for first impressions and repeat visits.

### Sports

**Sports hub** for browsing matches by context (sport, status, presentation) — built around a responsive, card-driven layout and clear CTAs toward streaming.

### Streaming

**Watch flow** with HLS-capable playback, source handling, and a UX focused on reliability (controls, fullscreen, live-oriented behaviour where applicable).

### Channels

**Channel directory and detail** — explore broadcasters / sources and drill into what’s relevant for a given channel.

### Search & match detail

**Search** across the experience; **match pages** anchor deep links so shares and bookmarks land on the right event.

### Trust & settings

**DMCA** transparency for a streaming-adjacent product; **settings** and theming so users control how the app feels (e.g. light/dark).

<p align="center">
  <img src="docs/about/screenshot-sports.png" alt="Sports view (add your screenshot)" width="640" /> 
  <img src="docs/about/screenshot-streaming.png" alt="Streaming / player (add your screenshot)" width="640" />
</p>

---

## Tech stack

| Layer | Technologies |
|--------|----------------|
| **Frontend** | Next.js (App Router), React, TypeScript, Tailwind CSS, PWA-oriented delivery |
| **Media** | Hls.js, adaptive streaming, custom video controls |
| **Backend** | NestJS, REST APIs, structured modules for matches, sync, and integrations |
| **Data** | PostgreSQL, persisted match/channel domain data where the architecture calls for it |
| **Ops** | Docker & Compose for reproducible local and deployable stacks |

*Stack evolves with the product — the constraint is maintainability, not hype.*

---

## What makes 8ein Sport unique?

1. **Design-first, execution-backed** — UI/UX is not an afterthought; performance and clarity are part of the feature set.
2. **Full-stack ownership** — one coherent vision from API contracts to player behaviour, without “handoff gaps.”
3. **Streaming-realistic** — HLS, fallbacks, and controls that match how people actually watch.
4. **Room to grow** — architecture supports swapping data sources, adding intelligence, and scaling features without rewriting the whole app.

---

## Architecture overview

```text
┌─────────────────────────────────────────────────────────────┐
│                        Client (PWA)                          │
│              Next.js · React · Tailwind · Hls.js             │
└───────────────────────────┬─────────────────────────────────┘
                            │ HTTPS / API routes
┌───────────────────────────▼─────────────────────────────────┐
│                     Backend (NestJS)                         │
│     Matches API · sync · integrations · health & ops         │
└───────────────────────────┬─────────────────────────────────┘
                            │
┌───────────────────────────▼─────────────────────────────────┐
│                   PostgreSQL + domain model                 │
└─────────────────────────────────────────────────────────────┘
```

- **Frontend** talks to **backend APIs** for real data flows; mock-friendly paths exist where useful for demos and design.
- **Containers** align environments so “works on my machine” isn’t a lottery.
- **Separation of concerns** keeps UI, API, and persistence testable and replaceable.

<p align="center">
  <img src="docs/about/diagram-custom.png" alt="Optional: your own architecture diagram" width="680" />
</p>

---

## Vision (where it’s headed)

The north star is a **single surface** that respects your time: **entertainment** (watch), **structure** (sports & channels), and eventually **smarter layers** (recommendations, assistance, and tools that feel native — not bolted on). Shipping that stack is iterative; what exists today is the foundation.

---

## For interviewers

- **This file (`README.md`)** is the **public product + engineering story** for the project (what you see first on GitHub).
- **Technical setup** (install, Docker, mocks, theme, VideoPlayer): **[`docs/DEVELOPMENT.md`](./docs/DEVELOPMENT.md)**.
- **Why you can’t “show only README” on a private repo** + **how to create a public overview repo**: **[`docs/REPO_VISIBILITY.md`](./docs/REPO_VISIBILITY.md)**.
- **Contact:** *[add your email or LinkedIn here]*

---

## Developer quick link

| Doc | Purpose |
|-----|--------|
| [`docs/DEVELOPMENT.md`](./docs/DEVELOPMENT.md) | Run locally, Docker, mocks, theme, VideoPlayer |
| [`docs/REPO_VISIBILITY.md`](./docs/REPO_VISIBILITY.md) | Private vs public, GitHub Pages facts, “brochure” repo steps |

---

*Image placeholders: add files under `docs/about/` or update paths above.*
