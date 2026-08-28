<div align="center">

# mitu

### Hold a key. Talk. It types.

100% on‑device voice dictation for macOS. Nothing leaves your Mac.

</div>

---

## Download

**[⬇︎ Download mitu.zip](https://github.com/lilmonsterbasu/mitu-download/releases/latest/download/mitu.zip)**

Works on macOS 12 or later, Apple Silicon **and** Intel (universal build).

---

## Install

1. **Unzip** `mitu.zip` (double‑click it in Finder). You get `mitu.app`.
2. **Move** `mitu.app` into your **Applications** folder.
3. **Clear the download flag** — the app isn't from the App Store, so macOS blocks it once. Open **Terminal** (`⌘ Space`, type "Terminal") and run:

   ```bash
   xattr -dr com.apple.quarantine /Applications/mitu.app
   ```

   Then double‑click `mitu.app`.

   <details>
   <summary>No Terminal? Do it in Finder / Settings instead</summary>

   - **Right‑click** `mitu.app` → **Open** → click **Open** in the dialog.
   - If there's no **Open** button:  → **System Settings** → **Privacy & Security**, scroll to *“mitu was blocked from use…”*, click **Open Anyway**, then **Open** on the confirm dialog.
   </details>

---

## Grant 3 permissions

mitu runs in the **menu bar** (no Dock icon — look for the 🎙️). On first use it asks for:

| Permission | How to grant | Why |
|---|---|---|
| **Microphone** | Click **Allow** on the prompt | Record your voice |
| **Speech Recognition** | Click **OK** on the prompt | Transcribe locally — nothing is sent to Apple or any server |
| **Accessibility** | **System Settings → Privacy & Security → Accessibility** → turn **mitu** on | Run the shortcut and paste text at your cursor |

If dictation says *“the on‑device speech model isn't ready”*: **System Settings → Keyboard → Dictation**, turn it on once so macOS downloads the offline model, then try mitu again.

---

## Use it

Default shortcut: the **right ⌥ (Option)** key.

| Action | How |
|---|---|
| **Push‑to‑talk** | **Hold** the shortcut, speak, **release** — text is typed where your cursor is |
| **Hands‑free** | **Double‑tap** (or one quick tap) — dictate as long as you want — **tap once** to stop |

Change the shortcut in the dashboard: menu bar → **Open mitu Dashboard** → *Shortcut*. Any key, a combo, or a single modifier works.

---

## Fixes

**Accessibility is switched on in Settings, but the shortcut or auto‑paste still don't work.**
Because the app is unsigned, replacing it with a new download leaves a dead entry in the Accessibility list. Reset it:

1. Menu bar → **Quit mitu**.
2. **System Settings → Privacy & Security → Accessibility** → select **mitu** → click **–** to remove it.
3. Make sure there's only **one** `mitu.app` — in `/Applications`. Delete any copy left in `~/Downloads`.
4. Reopen `/Applications/mitu.app` and turn Accessibility on again. If it still doesn't take, **quit and reopen** mitu once more.

**Nothing pastes, but the text is on the clipboard.** Auto‑paste needs Accessibility (above). Until then, press **⌘V**.

**Updating.** Download the new `mitu.zip`, replace `/Applications/mitu.app`, and redo the Accessibility reset above — once per update.

---

<div align="center">
<sub>This repo hosts the download only. The source is in a private repository.</sub>
</div>
