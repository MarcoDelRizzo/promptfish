# Promptfish 🐟♟️

**A bring-your-own-key chess coach that overlays Lichess & Chess.com — plus a desktop companion app for macOS and Windows.**

Promptfish adds a floating coach to the analysis, study, and review boards on
Lichess and Chess.com. Ask about any position, get move-by-move explanations,
and run a full game review with a color-coded evaluation graph and
move-classification breakdown — all powered by an AI model you choose and pay
for directly.

> **Fair play:** Promptfish only works on **analysis / study / review** surfaces.
> Live and ongoing games are blocked by design.

---

## What's in a release

Every [release](https://github.com/MarcoDelRizzo/promptfish/releases/latest) ships these downloads — grab whichever you need:

| File | What it is |
| --- | --- |
| `promptfish-extension-<version>.zip` | The **browser extension** — the overlay on Lichess & Chess.com. Works on its own. |
| `Promptfish-<version>-arm64.dmg` | The **macOS desktop app** (Apple Silicon). |
| `Promptfish Setup <version>.exe` | The **Windows desktop app** (Windows 10/11). |

You do **not** need the desktop app to use the extension — the extension alone is
the fastest way to start (bring your own API key). The desktop app is for coaching
**free with your own Claude Pro/Max subscription** (no API key needed).

---

## Install — Browser extension (Chrome, Edge, Brave)

1. Download **`promptfish-extension-<version>.zip`** from the [latest release](https://github.com/MarcoDelRizzo/promptfish/releases/latest).
2. Unzip it — you'll get an `extension` folder.
3. Open **`chrome://extensions`** (or `edge://extensions`, `brave://extensions`).
4. Turn on **Developer mode** (top-right toggle).
5. Click **Load unpacked** and select the unzipped **`extension`** folder.
6. Pin the Promptfish icon so it's easy to find.

---

## Install — Desktop app (macOS · Apple Silicon)

Requires an **Apple Silicon** Mac (M1 / M2 / M3 / M4), macOS 12 or later. Intel
Macs aren't built — use the browser extension instead.

1. Download **`Promptfish-<version>-arm64.dmg`** from the latest release.
2. Open the `.dmg` and drag **Promptfish** into your **Applications** folder.
3. Open it from Applications. The app is **signed with an Apple Developer ID and
   notarized**, so it opens with a normal double-click — no security workaround
   needed. *(If macOS ever asks on the very first launch, right-click the app →
   **Open** → **Open**.)*

From then on the app **updates itself automatically** in the background.

---

## Install — Desktop app (Windows 10 / 11)

Requires 64-bit **Windows 10 or 11**.

1. Download **`Promptfish Setup <version>.exe`** from the latest release.
2. Run it. The installer isn't code-signed yet, so **Windows SmartScreen** may show
   *"Windows protected your PC."* Click **More info → Run anyway**.
3. Follow the installer (you can choose the install folder). It adds a **Promptfish**
   Start-menu shortcut and launches the app.

From then on the app **updates itself automatically** in the background.

---

## Coaching for free with your Claude subscription (desktop app)

The desktop app can coach using **your own Claude Pro/Max** — no API key, no
per-message cost. You'll need **Claude Code** installed
(`npm i -g @anthropic-ai/claude-code`).

1. Install the desktop app (above) and open it.
2. In the extension popup, set the **engine** to **Claude Desktop**.
3. Coach:
   - **macOS:** just send a prompt in the overlay — Promptfish opens a Claude
     terminal for you and reuses it.
   - **Windows:** click **Connect Claude** in the app once, then send prompts.

Prefer to bring your own API key instead? You can skip the desktop app entirely and
just use the extension — see **First run** below.

---

## First run (extension + your own API key)

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

- **Desktop app (macOS & Windows):** updates **automatically** — it downloads new
  releases in the background and installs them the next time you quit. You'll see a
  small *"Promptfish updated"* note on the next launch.
- **Extension:** shows an *"update available → Download"* banner in the overlay.
  Download the new `promptfish-extension-<version>.zip`, then in `chrome://extensions`
  drop the new `extension` folder over the old one and hit **Reload** (or re-run
  *Load unpacked*).

---

## Troubleshooting

- **macOS asks to confirm on the first launch:** right-click the app → **Open** →
  **Open** (needed at most once; the app is notarized).
- **Windows SmartScreen warning:** **More info → Run anyway** — the installer just
  isn't code-signed yet.
- **Extension not showing on a game:** it's intentional — Promptfish stays off live
  games. Open the **Analysis** board for that game instead.
- **No coach responses:** double-check your API key and that your provider has
  credit/quota — or, in **Claude Desktop** mode, that Claude Code is installed and
  the Claude terminal is running.

---

Questions or issues? Open one on the [releases repo](https://github.com/MarcoDelRizzo/promptfish/issues).
