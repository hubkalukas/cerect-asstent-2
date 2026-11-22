# cerect asstent 2

Android overlay AI asistent pro rychlou analýzu obrazovky (kvízy, Kahoot, textové otázky) pomocí Google Gemini API.

## Hlavní funkce
- **Plovoucí rohové tlačítko (Stealth mód):** Jedním klepnutím sejme obrazovku přes `MediaProjection` a v rohu ukáže barevný symbol odpovědi (`▲` červená, `◆` modrá, `●` žlutá, `■` zelená) nebo červený indikátor `!` při chybě.
- **Podpora rotace (Portrait i Landscape):** Automatické přizpůsobení `VirtualDisplay` a `ImageReader` při otočení displeje.
- **Rychlý modelový pool bez umělých limitů v aplikaci:**
  1. `gemini-3.5-flash-lite` (primární — ~0,7 s, extrémně nízká cena)
  2. `gemini-3.1-flash-lite` (záloha Lite)
  3. `gemini-3.6-flash` (reasoning záloha)
  4. `gemini-3.8-flash` (nejvyšší Flash záloha)
- **Ochrana soukromí a bezpečnosti:** API klíč není uložen v tomto repozitáři a v aplikaci jej nelze zobrazit.

## Konfigurace vlastního API klíče
Tento repozitář **neobsahuje žádný API klíč**. Pro vlastní sestavení doplňte svůj Google AI Studio klíč lokálně do konfigurace aplikace (např. `AppPreferences` / `local.properties`) a nikdy jej necommitujte do Gitu.

## Struktura projektu
- `src/main/java/com/example/` — zdrojové soubory aplikace (`MainActivity`, `CornerOverlayService`, `ScreenCaptureManager`, `GeminiService`, `GeminiRateLimiter`, UI obrazovky)
