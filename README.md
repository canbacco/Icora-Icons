# Icora Icons

Icora Icons is a lightweight icon set powered by pure CSS and SVG masks. It requires no JavaScript and can be easily added to any project.

## Features

- Pure CSS implementation  
- No runtime JavaScript required  
- Scalable and lightweight  
- Easy to integrate into any web project

## Getting Started
1. Include the stylesheet:
```html
<link rel="stylesheet" href="icora.css" />
```
2. Add the desired icon class:
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

## Add Your Own Icons
Convert your SVGs to Data URIs and create classes under the “Icons” section in `icora.css`:
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

## Available Icons (in this repo)
- `icora-chevron-left`
- `icora-chevron-up`
- `icora-chevron-right`
- `icora-chevron-down`
- `icora-filter-o`
- `icora-filter-f`
- `icora-person-add-o`
- `icora-login-o`

## Tips & Troubleshooting
- If an icon doesn’t show, ensure the element has color (icons use `background-color: currentColor`).
- Ensure your SVG has a `viewBox` (add one if missing).
- Prefer simple strokes/fills; masks rely on shape opacity (color is ignored in masks).
- Data URIs should include `charset=utf-8` for robust cross-browser handling.

## Contributing
PRs welcome. If you add icons, include:
- The CSS block in `icora.css`
## License
MIT


