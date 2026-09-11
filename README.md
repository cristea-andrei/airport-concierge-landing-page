# Valet 24 — airport valet (landing page)

Landing page for Valet 24, a meet-and-greet valet service at Bucharest's two airports:
Otopeni (OTP, Henri Coandă) and Băneasa (BBU, Aurel Vlaicu). The driver takes
the car at Departures and brings it back to Arrivals on return.

## Files

- `index.html` — the whole site. No build step, no dependencies to install.
- `assets/hero.webp` — the hero photograph (1100px, 95 KB).

Open it by double-clicking, or serve it locally:

```
python3 -m http.server 8000    # then open http://localhost:8000
```

## What's in it

- Romanian by default, English via the RO/EN toggle in the header. The choice is
  remembered in the browser; visitors on a non-Romanian browser get English first.
- Booking by phone (`tel:` link) and on WhatsApp (`wa.me/40741220600`), both on
  +40 741 220 600. Plain links, no prefilled message.
- Icons come from the Lucide and Simple Icons packages, inlined as an SVG sprite
  so the page has no runtime dependency on a CDN.
- The hero photograph is AI-generated. Replace it with a real photo of your own
  drivers and cars once you have one — swap the file at `assets/hero.webp` and
  keep the name, no markup change needed.
- Fonts: Bodoni Moda, Archivo and IBM Plex Mono, loaded from Google Fonts.

## Changing the text

Romanian copy lives in the markup. English lives in the `EN` object in the
script at the bottom, keyed by the `data-i18n` attribute on each element. Change
one, change the other to match.

The phone number appears in `tel:` links and as visible text — search for
`741220600` and `741 220 600` to catch every instance.
