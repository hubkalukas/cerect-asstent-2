# cerect asstent 2

![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?logo=android&logoColor=white)
![AI](https://img.shields.io/badge/AI-Google%20Gemini%20API-4285F4?logo=googlegemini&logoColor=white)
![Release](https://img.shields.io/github/v/release/hubkalukas/cerect-asstent-2?label=Release)

Android overlay AI asistent pro rychlou analýzu obrazovky (kvízy, Kahoot, textové otázky) pomocí Google Gemini API.

> **English summary:** Lightweight Android floating-overlay AI screen assistant using `MediaProjection` and Google Gemini API. Supports Portrait & Landscape rotation, stealth corner indicators, multi-model fallback, and bring-your-own API key (no keys stored in this repo).

---

## ⬇️ Stažení a instalace

- **[Stáhnout cerect_asstent_2.apk (nejnovější verze)](https://github.com/hubkalukas/cerect-asstent-2/releases/latest/download/cerect_asstent_2.apk)**
- Další verze a poznámky najdeš v sekci [Releases](https://github.com/hubkalukas/cerect-asstent-2/releases).

---

## Hlavní funkce

- **Plovoucí rohové tlačítko (Stealth mód):** Jedním klepnutím sejme obrazovku přes `MediaProjection` a v rohu zobrazí barevný symbol odpovědi (`▲` červená, `◆` modrá, `●` žlutá, `■` zelená) nebo červený indikátor `!` při chybě.
- **Podpora rotace (Portrait i Landscape):** Automatické přizpůsobení `VirtualDisplay` a `ImageReader` při otočení displeje.
- **Modelový pool se zálohou bez umělých limitů v aplikaci:**
  1. `gemini-3.5-flash-lite` (primární — ~0,7 s, extrémně nízká cena)
  2. `gemini-3.1-flash-lite` (záloha Lite)
  3. `gemini-3.6-flash` (reasoning záloha)
  4. `gemini-3.8-flash` (nejvyšší Flash záloha)
- **Soukromí a bezpečnost:** V tomto repozitáři není uložen žádný API klíč a v aplikaci jej nelze zpětně zobrazit.

---

## Konfigurace vlastního API klíče

Tento repozitář **neobsahuje žádný API klíč**. Pro vlastní sestavení doplň svůj klíč z [Google AI Studio](https://aistudio.google.com/) lokálně do konfigurace aplikace (např. `AppPreferences` / `local.properties`) a nikdy jej necommituj do Gitu.

## Struktura projektu

Zdrojové soubory jsou zabalené v `cerect-asstent-2-source.zip`:
- `src/main/java/com/example/` — `MainActivity`, `CornerOverlayService`, `ScreenCaptureManager`, `GeminiService`, `GeminiRateLimiter` a UI obrazovky.

> **Související projekt:** Webovou verzi pro PC najdeš v repozitáři [hubkalukas/ai](https://github.com/hubkalukas/ai).