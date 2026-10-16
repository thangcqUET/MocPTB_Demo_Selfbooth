# The Era booth — brand spec (demo skin)

A second brand skin for the Selfbooth prototype. Same components, same
layout, same end-to-end flow as the default Poze system — only the token
layer changes, bound as `html[data-brand="the-era"]` in `index.html`.
Switch by appending `?brand=the-era` to the prototype URL.

Authoring brief: `The Era booth`, palette beige + light wood, modern type,
Poze-style function screens, no AI slop.

## One-sentence system

Warm light-beige canvas, light-wood surfaces used structurally (device
bezels, staff/admin sidebar), one deep-caramel accent, and a single modern
geometric sans (Manrope) carrying all hierarchy — no condensed or rounded
display face.

## Color tokens (hex; OKLch where derived)

| token | hex | role |
|---|---|---|
| `--bg` | `#f3ebdd` | beige page + app canvas |
| `--bg-deep` | `#eadcc4` | recessed panels, admin main, letterbox |
| `--bg-ink` | `#c3a377` | **light wood** — device bezels, staff/admin sidebar |
| `--island` | `#241a10` | phone cut-out (stays dark on the wood bezel) |
| `--surface` | `#fbf7ee` | warm near-white cards, inputs, keys |
| `--surface-2` | `#f0e7d6` | pressed / secondary cream |
| `--fg` | `#3a2c1d` | espresso text on beige |
| `--ink` | `#2b2014` | ink text on surface |
| `--muted` | `#7c6647` | secondary text on beige |
| `--muted-ink` | `#8a7458` | secondary text on surface |
| `--border` | `#ddcbb0` | hairline on beige |
| `--border-ink` | `#e3d4ba` | hairline on surface |
| `--accent` | `#a9742f` | **deep caramel** — wordmark, headline, countdown ring, primary pill |
| `--accent-2` | `#8a5a24` | darker wood — eyebrows, subheads, hover |
| `--gold-deep` | `#8a5a24` | caramel pressed |
| `--ok` | `#3f9d6a` | confirm / print / tiếp tục |
| `--danger` | `#c5452f` | cancel / chụp lại / hủy |
| `--info` | `#4f7aa8` | next / đổi frame / quay lại |
| `--orange` | `#c07a34` | coaching hint pill |
| `--oncam` | `#fbf7ee` | light text over the dark camera photo |

The printed-frame artwork palettes (`--frame-coastal-*`, `--frame-catba-*`,
`--frame-love-*`) are content, not chrome — they are unchanged.

## Type

| token | stack | use |
|---|---|---|
| `--font-display` | `'Manrope', 'Be Vietnam Pro', system-ui, sans-serif` | headings, big numbers — weight **800** |
| `--font-round` | `'Manrope', 'Be Vietnam Pro', system-ui, sans-serif` | labels, pills, buttons, subheads |
| `--font-serif` | `'Manrope', 'Be Vietnam Pro', system-ui, sans-serif` | wordmark only |
| `--font-body` | `'Be Vietnam Pro', system-ui, sans-serif` | body, admin tables |
| `--font-mono` | `'Manrope', 'Be Vietnam Pro', system-ui, sans-serif` | queue no., session code, price, order id (tabular figures) |

Every tier collapses to **one** family. Manrope (`400–800`) drives all
hierarchy by weight and tracking; Be Vietnam Pro carries body copy. The
default system's Anton (condensed) + Baloo 2 (rounded) + Bodoni Moda
(serif) + system mono are all collapsed to Manrope. The Poze
condensed-uppercase treatment is dropped — display headings render in
sentence case at weight 800.

## Layout posture (observed / intended)

1. **Light canvas, dark text** — every chrome token is remapped so text on
   beige and text on cream are both espresso/ink. No inversion per surface.
2. **Wood is structural** — the light-wood tone (`#c3a377`) lives in the
   phone bezel, the staff/admin sidebar, and the **nav + active states**
   (active rail item, hover, sidebar selection wash). No raw hex is used
   outside the `:root` / `html[data-brand="the-era"]` token blocks — the
   camera flash reads `var(--flash)`.
3. **One accent** — deep caramel carries the wordmark, the section headline,
   the countdown ring and the single primary pill. Status colors never decorate.
4. **Weight-driven hierarchy** — Manrope 800 for display, 600–700 for labels.
   No letter-spacing tricks, no condensed uppercase stack.
5. **Camera chrome flips** — over the dark capture photo, overlay chips and
   shutter labels switch to `--oncam` (light) so they stay legible.

## How to switch

```
# default Poze skin
…/index.html

# The Era booth skin
…/index.html?brand=the-era
```

The brand param drives: the token block above, the wordmark (`THE ERA`),
the topbar subtitle, the phone / booth / sidebar labels, the session-link
domain (`theera.vn`), the footer, and the document title.
