# Promptfish 🐟♟️

**A bring-your-own-key chess coach that overlays Lichess & Chess.com — plus a macOS companion app.**

Promptfish adds a floating coach to the analysis, study, and review boards on
Lichess and Chess.com. Ask about any position, get move-by-move explanations,
and run a full game review with a color-coded evaluation graph and
move-classification breakdown — all powered by an AI model you choose and pay
for directly.

> **Fair play:** Promptfish only works on **analysis / study / review** surfaces.
> Live and ongoing games are blocked by design.

---

## What's in a release

Every [release](https://github.com/MarcoDelRizzo/promptfish/releases/latest) ships two downloads — grab whichever you want (or both):

| File | What it is |
| --- | --- |
| `promptfish-extension-<version>.zip` | The **browser extension** — the overlay on Lichess & Chess.com. |
| `Promptfish-<version>-arm64.dmg` | The **macOS desktop app** (Apple Silicon) — bundles the coach server and connects Promptfish to Claude Desktop / Claude Code. |

You do **not** need the desktop app to use the extension. The extension alone is
the fastest way to start.

---

## Install — Browser extension (Chrome, Edge, Brave)

1. Download **`promptfish-extension-<version>.zip`** from the [latest release](https://github.com/MarcoDelRizzo/promptfish/releases/latest).
2. Unzip it — you'll get an `extension` folder.
3. Open **`chrome://extensions`** (or `edge://extensions`, `brave://extensions`).
4. Turn on **Developer mode** (top-right toggle).
5. Click **Load unpacked** and select the unzipped **`extension`** folder.
6. Pin the Promptfish icon so it's easy to find.

## Install — Desktop app (macOS, Apple Silicon)

1. Download **`Promptfish-<version>-arm64.dmg`** from the latest release.
2. Open the `.dmg` and drag **Promptfish** into **Applications**.
3. First launch only: the app is unsigned, so macOS will warn. **Right-click the
   app → Open → Open.** (Or allow it under *System Settings → Privacy & Security →
   Open Anyway*.) After that it opens normally.

> The DMG is Apple-Silicon only. Intel Macs aren't built yet — use the browser
> extension instead.

---

## First run

1. Open a **Lichess or Chess.com analysis / study / review board** (not a live game).
2. Click the floating **Promptfish** widget on the page.
3. Add your **API key** — Promptfish is bring-your-own-key. It works with:
   - **OpenRouter** or **Groq** (both have free tiers — easiest start)
   - **Anthropic** (Claude), **OpenAI**, or any OpenAI-compatible endpoint
   - a **local model** (e.g. Ollama)

   Your key is stored locally in your browser and is only ever sent to the API
   endpoint you configure — never to us.
4. Pick a **coach personality** and analysis depth, then ask about the position —
   or open **Game Review** to analyze a whole game with an evaluation graph and a
   per-move breakdown.

---

## Staying up to date

Promptfish checks this repository for new releases automatically:

- the **extension** shows an *"update available → Download"* banner in the overlay,
- the **desktop app** pops a one-time *"Update available"* dialog.

When you see it, download the new file and reload:

- **Extension:** re-run *Load unpacked* on the new `extension` folder (or drop it
  over the old one and hit **Reload** in `chrome://extensions`).
- **Desktop:** open the new `.dmg` and replace the app in Applications.

---

## Troubleshooting

- **"Promptfish is damaged / can't be opened" (macOS):** this is the unsigned-app
  warning — right-click the app → **Open**, or allow it in *Privacy & Security*.
- **Extension not showing on a game:** it's intentional — Promptfish stays off
  live games. Open the **Analysis** board for that game instead.
- **No coach responses:** double-check your API key and that your provider has
  credit/quota.

---

Questions or issues? Open one on the [releases repo](https://github.com/MarcoDelRizzo/promptfish/issues).
