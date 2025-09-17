# Icora CSS Icon Library

Pure CSS icon library that paints SVG paths via CSS masks. No runtime JavaScript required. Icons inherit color from text using `currentColor`, scale with `font-size`, and align neatly with text baselines.

## Features
- Zero JS at runtime – just include one CSS file
- Color via `currentColor` (change icon color with regular CSS)
- Crisp sizing with `font-size` or utility classes (`.icora-xs/sm/md/lg`, `.icora-1x…5x`)
- Baseline alignment for inline text; fixed-width option for list layouts
- Works with inline Data URIs
- Ships both `-webkit-mask-image` and `mask-image` for broad browser support

## Getting Started
1. Include the stylesheet:
```html
<link rel="stylesheet" href="css/icora.css" />
```
2. Use an icon class:
```html
<i class="icora icora-filter-o"></i>
```
3. Color and size with regular CSS:
```html
<!-- Inherit color -->
<p style="color:#7c3aed"><i class="icora icora-filter-o"></i> Filter</p>

<!-- Size with font-size or utilities -->
<i class="icora icora-filter-f" style="font-size:24px"></i>
<i class="icora icora-filter-f icora-2x"></i>
```

## Utilities
- `.icora-fw`: fixed width for neat columns in menus/lists
- Size helpers (scale via `font-size`):
  - `.icora-xs`, `.icora-sm`, `.icora-md`, `.icora-lg`
  - `.icora-1x`, `.icora-2x`, `.icora-3x`, `.icora-4x`, `.icora-5x`

Example:
```html
<ul>
  <li><i class="icora icora-fw icora-filter-o"></i>Filter</li>
  <li><i class="icora icora-fw icora-person-add-o"></i>Add person</li>
</ul>
```

## Available Icons (in this repo)
- `icora-filter-o`
- `icora-filter-f`
- `icora-person-add-o`
- `icora-login-o`

Use them like:
```html
<i class="icora icora-login-o"></i>
```

## Add Your Own Icons
Convert your SVGs to Data URIs and create classes under the “Icons” section in `css/icora.css`:
```css
.icora-your-icon { -webkit-mask-image: url("data:image/svg+xml;charset=utf-8,..."); mask-image: url("data:image/svg+xml;charset=utf-8,..."); }
```

 

## Accessibility
- Decorative icons: add `aria-hidden="true"` or mark the container as presentational.
- Meaningful icons: add `role="img"` and an `aria-label` describing the icon.

Examples:
```html
<i class="icora icora-filter-o" aria-hidden="true"></i>
<span role="img" aria-label="Login"><i class="icora icora-login-o"></i></span>
```

## Browser Support
CSS mask support is available in modern browsers:
- Chromium-based (Chrome, Edge), Safari (including iOS), Firefox (partial for mask properties)
- Not supported in Internet Explorer

Use the provided pair of properties for best coverage:
- `-webkit-mask-image` (WebKit/Blink)
- `mask-image` (standard)

## Tips & Troubleshooting
- If an icon doesn’t show, ensure the element has color (icons use `background-color: currentColor`).
- Ensure your SVG has a `viewBox` (add one if missing).
- Prefer simple strokes/fills; masks rely on shape opacity (color is ignored in masks).
- Data URIs should include `charset=utf-8` for robust cross-browser handling.

## Contributing
PRs welcome. If you add icons, include:
- The CSS block in `css/icora.css`
- Optional source SVGs in `svgs/`

## License
MIT
