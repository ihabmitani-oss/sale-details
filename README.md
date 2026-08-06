# Sale Details — Almosafer HUB Sale Page Revamp v2

A production-ready, self-contained implementation of the **Sale Page Revamp v2**
design (Almosafer HUB — Unify Sale page), built from the Claude Design mockup.

The Sale page is the agent workspace for a sale file: customer info, cart,
confirmed bookings (hotel / flight), payments, and summary — with the sale
locking, cancellation, refund, and invoice flows.

## Running

No build step and no dependencies (fonts load from Google Fonts). Just open the
file, or serve the folder:

```bash
open index.html
# or
python3 -m http.server 8000   # then visit http://localhost:8000
```

## What's inside

`index.html` — the entire page: markup, styles, and a small vanilla-JS state
machine (ported from the design's `DCLogic` component). Interactions wired up:

- Expandable sidebar navigation (collapsed rail ↔ open panel)
- "With bookings" ↔ "Fresh sale" states across Bookings / Payments / Summary
- Lock / Unlock sale (with locked banner and disabled actions)
- Editable "Current Sales Office" (summary strip + cart header)
- Contact inline edit, and the Link-customer → error → edit & retry → linked flow
- Hotel / Flight booking accordions, detail tabs, and Order/Product notes toggle
- Guarded booking cancellation (confirmation modal), refund modal, invoice generation

## Design system

Colors and type are transcribed from the Almosafer Hub design-system tokens, with
the aqua (`#0C9AB0`) brand override applied. The Almosafer logo is currently a
styled text wordmark placeholder — swap in the real SVG when available.
