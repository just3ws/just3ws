# Mike Hall

**Development Manager.** I build teams that ship observable, PHI-safe systems — and I stay close enough to the code to know when something's wrong before the alerts do.

Previously Staff/Principal Engineer. Now focused on making the engineers around me faster and the systems they build more legible.

---

## What I'm working on

Starting as **Development Manager at EMR-Bear** — bringing engineering discipline to healthcare infrastructure where correctness isn't optional and PHI compliance is a hard constraint, not an afterthought.

---

## 🎙️ The UGtastic & SCMC Oral History Archive (2009–2026)

Curating 15 years of oral history and engineering wisdom across Midwest software craftsmanship movements (Software Craftsmanship North America, Chicago ALT.NET, RailsConf 2014, GOTO Chicago):

- 📜 **100% Transcribed Corpus:** 207 video interviews (~456k words) with vector search (`zdots-ctx`).
- 🕸️ [**Charlotte's Web of Wisdom & Tributes**](https://www.just3ws.com/web/) — 184 glowing speaker tributes & craftsmanship principles.
- 💎 [**Archive Curiosities & Hidden Gems**](https://www.just3ws.com/curiosities/) — Tech prophecies vs. 2026 reality & lost tooling history.
- 📊 [**Archive Pattern Intelligence**](https://www.just3ws.com/intelligence/) — Interactive trope visualizer & corpus heatmaps.
- 🗺️ [**Interactive Timeline**](https://www.just3ws.com/timeline/) & [**Speaker Directory**](https://www.just3ws.com/speakers/)

---

## The stack

```
Inference      llama.cpp · speculative decoding (Qwen3-8B + 0.6B draft) · local-only
Observability  OpenTelemetry · Grafana LGTM stack · shell-level tracing
Backend        Ruby / Rails · PostgreSQL · Sequel · dry-monads
Shell          zsh · zdots platform · 22-test eval suite · PHI scrubbing pipeline
Infra          Colima · nginx · mkcert · launchd · mise
Security       PHI pattern registry · locality assertions · keychain-only secrets
```

---

## The dots

My local environment is a set of version-controlled, reproducible configuration repos. Cold restore from a single command:

```bash
git clone https://github.com/just3ws/zdots.git ~/.config/zsh && ~/.config/zsh/bin/bootstrap
```

| Repo | Path | What it is |
|------|------|------------|
| [**zdots**](https://github.com/just3ws/zdots) | `~/.config/zsh` | Shell platform. OTel tracing, local AI routing, PHI scrubbing, test suite. Drives bootstrap. |
| [**adots**](https://github.com/just3ws/adots) | `~` | Dotfiles monorepo. git config, tmux, bat, btop, lazygit — everything that isn't a platform. |
| [**vdots**](https://github.com/just3ws/vdots) | `~/.config/nvim` | Neovim. LSP, treesitter, Ruby/Go/TypeScript tooling. |

The shell platform runs a [Message Hygiene Pipeline](https://github.com/just3ws/zdots) — every prompt through normalize → PHI scrub before it touches inference. Pattern registry is a single YAML file consumed by both the bash sed scrubber and the Ruby `PhiScrubber`. One edit, full coverage.

---

## What "observable systems" means here

Shell commands emit OpenTelemetry spans. The local LGTM stack (Loki, Grafana, Tempo, Mimir) ingests them. The morning briefing queries real trace data, not vibes.

Inference calls are locality-asserted: the AI boundary exits hard if the endpoint isn't loopback or RFC-1918. No accidental cloud egress from a work machine.

---

## Writing and thinking

> *"Complex systems become understandable when you stop hiding their behaviour and start instrumenting it."*

I write about shell engineering, local AI infrastructure, building observable systems, and preserving software engineering history. Website: [just3ws.com](https://www.just3ws.com)

---

<div align="center">

[![GitHub Stats](https://github-readme-stats.vercel.app/api?username=just3ws&show_icons=true&theme=dracula&hide_border=true&count_private=true)](https://github.com/just3ws)
&nbsp;&nbsp;
[![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=just3ws&layout=compact&theme=dracula&hide_border=true)](https://github.com/just3ws)

</div>
