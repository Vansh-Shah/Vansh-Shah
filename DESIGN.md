# Design

The Jas Enterprise landing page (`index.html`). Visual language: the "Dyson" style from styles.refero.design (an engineering gallery on warm paper), laid out with the taste-skill "specimen catalogue" direction. Single light theme by choice.

## Colour

| Token | Value | Use |
| --- | --- | --- |
| `--canvas` | `#fff8e6` | Page ground, the gallery mat |
| `--paper` / `--paper-2` | `#ffffff` / `#faf5e8` | Range section ground and alternating rows |
| `--ink` / `--ink-soft` | `#333333` / `#555555` | Text / secondary text |
| `--lintel` | `#000000` | Header bar, trade-show band, footer |
| `--signal` / `--signal-deep` | `#0066cc` / `#0a55a8` | Links; the contact field and its input cells |
| `--go` | `#3d7a0c` | The one action colour (Dyson green, deepened for 4.5:1 with white) |
| `--ember` | `#8a4a00` | "New" and "Updated" labels only |
| `--t-sage`, `--t-sand`, `--t-mist`, `--t-paper` | `#e3ead6`, `#f3e4d0`, `#e6ecf3`, `#ffffff` | Specimen tile fields, rotated per machine |

No gradients, no shadows, no hairline rules. Surfaces are separated by tone steps.

## Type

One family: Jost (Futura substitute) at 300 / 400 / 500. Five sizes only:
14 (`--s-small`), 17 (`--s-body`), 22 (`--s-item`), 28–36 (`--s-head`), 52–132 (`--s-display`).
Headlines weight 300, tracking -0.02 to -0.035em, never more than two lines.

## Shape and space

- One radius: 2px, on buttons, inputs and tiles.
- Buttons: filled rectangles, 48px tall (40px in the header), `scale(0.97)` on press.
- One pair of page margins: `clamp(16px, 2.5vw, 32px)`, plus safe-area insets. 12-column grid, 24px gutter.
- Sections 96–176px apart.

## Components

- **Lintel header**: black bar, wordmark, four links, green "Send an enquiry".
- **Specimen picker** (hero): a 4:5 tile holding one machine photo (`mix-blend-mode: multiply`), a name list beside it. Choosing a name swaps photo, tile colour and fact with a blurred crossfade; it auto-cycles every 5.6s until the visitor picks one.
- **Two fields** ("New on the line"): two flat panels, each with one machine cropped by the top edge.
- **Range list**: 18 full-width rows in alternating tones; a machine cut-out rides down the centre (sticky) on desktop.
- **Printed invitation**: a tilted cream card on black, cut off by the section edge, for the trade show.
- **Contact field**: signal blue, a scroll-linked photo strip, a three-cell enquiry bar that opens a pre-filled email, four named sales lines.
- **Postcard footer**: scalloped cream card with address, a stamp photo, and the name at display size.

## Motion

Custom curves: `--ease-out: cubic-bezier(0.23, 1, 0.32, 1)`, `--ease-in-out: cubic-bezier(0.77, 0, 0.175, 1)`.
Reveals arm only below the first screen and only when script runs. Hover effects are gated behind `(hover: hover) and (pointer: fine)`. Under reduced motion: no auto-cycle, no travel, opacity only.

## Imagery

Product photographs are hotlinked from `https://www.jasenterprise.com/images/…` (the company's own). Every picture slot falls back to the machine's name on a tile if the photo fails to load.
