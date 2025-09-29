# BlueWave Tech — Product Landing Page

Modern, responsive landing page for a smart speaker with bilingual support (EN/AR), gallery with snapping and dots, lightbox, pricing offer, related items, and WhatsApp order form.

## Preview
- Open `index.html` directly in your browser, or serve the folder with any static server.

```bash
# Option A: VS Code Live Server / any static server
# Option B: Python
python -m http.server 8080
# then open http://localhost:8080/
```

## Project Structure
- `index.html` — markup and minimal JS for language toggle, gallery, lightbox, and WhatsApp form
- `style.css` — dark theme styles, sections, responsive rules
- External assets — Unsplash images and YouTube embed (attribution per their terms)

## Key Features
- Sticky top navigation with logo and quick links
- Hero with CTAs and language toggle (Arabic default)
- Scrollable image gallery with snap, arrows, and pagination dots
- Lightbox modal (click any gallery/product image)
- Promo video (responsive YouTube iframe)
- Feature cards, stats, pricing (50% OFF in EGP), related items
- Order form that opens WhatsApp with a prefilled message

## Configuration

1) Default Language
- Arabic is set as default.
- To change: in `index.html` update `<html lang="...">` and `<body class="...">`, or call `switchLang('en')` on load.

2) WhatsApp Order Number
- In `index.html`, find:
```js
const to = '201009884619';
```
- Replace with your international format (country code + number, no `+`).

3) Video URL
- In `index.html` under the video section, replace the YouTube `src` with your video ID:
```html
<iframe src="https://www.youtube.com/embed/VIDEO_ID?rel=0&modestbranding=1" ...></iframe>
```

4) Images
- Product scroller: edit the `<img>` tags inside `#productImages`.
- Gallery: edit `<section class="gallery">` images.
- Related items: edit cards inside `#related`.

5) Pricing
- In the pricing section, change the numbers in:
```html
<div class="price egp">
  <span class="now">EGP 999</span>
  <span class="old">EGP 1,998</span>
</div>
```

## Lightbox Controls
- Click image to open
- Arrow keys ←/→ to navigate, Esc to close
- Tap outside image to close on mobile

## Accessibility Notes
- Language attributes update (`<html lang>`)
- Buttons use `aria-label` where needed
- High-contrast focus styles via visual emphasis on interactive elements

## Browser Support
- Modern evergreen browsers. Snap scrolling and masks degrade gracefully.

## License
- Code: MIT
- Images and videos: subject to their original licenses (Unsplash/YouTube). Replace with your own assets for production.


