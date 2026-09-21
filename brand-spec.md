# Selfbooth — brand spec (extracted from Poze Overhead screens)

Source: `Poze Overhead screen 1920x1080 v1/*.png` (style) + `Mộc Selfbooth app screenshot/`, `Mộc Photobooth app screenshot/` (flow + component language).
Extraction method: sampled hex from the PNGs, read type posture and component radii off the screens.

## One-sentence system
Deep oxblood canvas with a faint film grain, one gold accent for brand + primary actions, cream surfaces for inputs and cards, and status green/red/blue reserved for confirm / cancel / next.

## Color tokens (OKLch, hex fallback)

| token | hex | role |
|---|---|---|
| `--bg` | `#7a1e22` | oxblood page canvas (kiosk + page) |
| `--bg-deep` | `#5c1417` | recessed panels, letterbox around camera |
| `--surface` | `#f7f1e3` | cream cards, inputs, keypad keys |
| `--surface-2` | `#efe6d2` | cream pressed / secondary |
| `--fg` | `#f6efe1` | cream text on oxblood |
| `--ink` | `#201d18` | ink text on cream |
| `--muted` | `#c9b49a` | secondary text on oxblood |
| `--muted-ink` | `#6d6355` | secondary text on cream |
| `--border` | `#a24e50` | hairline on oxblood |
| `--border-ink` | `#d9cdb4` | hairline on cream |
| `--accent` | `#c6a15b` | **gold** — logo, key headline, primary pill |
| `--accent-2` | `#ecd9a6` | pale gold — subheads, hover |
| `--gold-deep` | `#a9853f` | gold pressed |
| `--ok` | `#43b25a` | confirm / print / tiếp tục |
| `--danger` | `#e0402f` | cancel / chụp lại / hủy |
| `--info` | `#5b7fc7` | next / đổi frame / quay lại |
| `--orange` | `#e07b3a` | coaching hint pill ("bấm vào ảnh…") |

## Type

| token | stack | use |
|---|---|---|
| `--font-display` | `'Anton', 'Archivo Narrow', 'Oswald', sans-serif` | kiosk headlines — condensed heavy caps |
| `--font-round` | `'Baloo 2', 'Nunito', system-ui, sans-serif` | Vietnamese subheads, buttons, app labels |
| `--font-serif` | `'Bodoni Moda', 'Playfair Display', Georgia, serif` | `PÓZE` wordmark only |
| `--font-body` | `'Be Vietnam Pro', -apple-system, system-ui, sans-serif` | body, admin tables |
| `--font-mono` | `ui-monospace, 'SF Mono', Menlo, monospace` | queue no., session code, price, order id |

## Layout posture (observed)
1. **Bilingual always** — bold condensed/caps English line, rounded Vietnamese line beneath it, same size step.
2. **Pills, not rectangles** — primary buttons are fully rounded cream/gold pills with a 2px ink outline; gold = primary, cream = secondary.
3. **Dark rounded cards** on the oxblood canvas; inputs are cream pills with an ink outline.
4. **Gold budget** — gold carries the wordmark, the section headline, and the single primary action. Status colors never decorate.
5. **Camera stage** — black/white geometric-maze backdrop, letterboxed by blurred side panels, `LIVE` badge, big blue countdown ring.
6. **Star doodles + grain** — faint gold 4-point stars and a fine grain sit behind everything at low opacity; never in front of content.
