## MS Teams Live Captions Saver

Chrome extension that captures, previews, and saves live captions from the Microsoft Teams web interface. Supports multiple export formats, meeting history, and built‑in English→Russian translation powered by Yandex Translate.

### Features
- Automatic capture of captions and attendee lists.
- Real-time viewer with search, speaker filters, and analytics.
- Export of the visible transcript selection to TXT/Markdown.
- History of up to 10 sessions with instant load in the standalone Viewer.
- Integrated translation tab (“Original / Translation”) with a one-click “Translate” action.

### Installation
1. Open `chrome://extensions` in Chrome and enable **Developer mode**.
2. Click **Load unpacked** and select the project folder.
3. Copy `config.example.js` → `config.js`, then replace `YANDEX_TRANSLATE_API_KEY` with your own key (obtain it in the Yandex Translate console). Keep `config.js` out of Git—only the example file is tracked.
4. Reload the extension so the new settings take effect.

### Usage
- During a Teams call, open the popup and press **Start Capture**.
- **View Transcript** opens `viewer.html`, where you can search, copy, save, and translate.
- Press **Перевести / Translate** to trigger Yandex translation; the result appears under the **Translation (RU)** tab.
- Meeting history is available via the **History** button in the Viewer.

### Viewer Shortcuts
- `Ctrl/Cmd + F` — focus the search bar.
- `Esc` (while search is focused) — clear the current filter.

### Project Structure
- `content_script.js` — extracts captions directly from the Teams page.
- `service_worker.js` — background tasks and file saving.
- `popup.html/js` — control surface for capture and settings.
- `viewer.html/js` — dedicated window for browsing, filtering, and translation.
- `sessionManager.js` — manages persisted meeting history.

