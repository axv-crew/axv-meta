# AXV Pulse — Crew Guide (v1.1, PL)

**Cel:** jeden, krótki „puls” dziennie od załogi (Aster, Claude, Rezon, CLI, Wojtek) do `AXV_PULSE.md`. Najnowsze wpisy ZAWSZE na górze.

## Zasady (must)
- **Public repo → ZERO sekretów/PII.** Żadnych tokenów, haseł, IP WAN, telefonów itp.
- **Format wpisu:** `## <ISO-8601 z TZ> — <who>` + 3–5 punktorów (każdy = 1 myśl, max 1 linia).  
  Przykład nagłówka: `## 2025-11-10T16:00:00+01:00 — Aster`
- **`who` (ustandaryzowane):** `Aster`, `Claude`, `Rezon`, `CLI`, `Wojtek`. Emoji opcjonalne.
- **Linkuj PR/Issue**, gdy dotyczy (`#123`, `axv-web@abcdef1`).
- **Kolejność:** dopisujemy NA GÓRĘ pliku (prepend).

## Kiedy
- **Stały „Pulse” o 16:00** (codziennie).  
- **On-demand** przy ważnych zdarzeniach (merge, deploy, alert).  
- **Wieczorem 21:15** – krótki TL;DR ostatnich 24h (Aster do Wojtka).

## Jak wysłać (Webhook n8n → GitHub PUT /contents)
**Endpoint:** `POST …/webhook/aster/pulse/update`  
**Body (JSON):**
```json
{
  "who": "Aster",
  "ts": "2025-11-10T16:00:00+01:00",
  "lines": [
    "FE: NodeStatusBar na mocku OK",
    "API: OpenAPI v0.1 w repo",
    "Infra: route /api/axv/* na staging"
  ]
}
