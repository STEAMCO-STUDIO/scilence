# @scilence/tokens

Foundation design tokens for all STEAMCO products. These are the canonical source of truth — all product-specific token files (admin-tokens.css, site.css) should derive from or align with these values.

## Token Categories

| File | Contents |
|------|----------|
| `_palettes.css` | Color primitives: tealscale, greenscale, creamscale, brandscale (dynamic), brand-secondary, accent colors |
| `_spacing.css` | Fibonacci spacing scale (3-55px), density multiplier, semantic layout tokens |
| `_typography.css` | Font families, modular size scale, weights, line heights, density modes |
| `_radius-borders.css` | Proportional radius (font-size derived) and border width system |
| `_z-index.css` | Z-index ladder (base through max) |
| `_shadows.css` | Shadow scale (sm-xl), icon size tokens |
| `_transitions.css` | Duration, easing, transition shorthands, component-specific transitions |
| `_status-colors.css` | Success, warning, danger, info with bg/border/fg variations |
| `_prominent.css` | Prominent action colors and on-color foregrounds |
| `_alpha-overlays.css` | White (lift) and black (dark) alpha overlay tokens |

## Usage

```css
@import '@scilence/tokens/src/index.css';
```

Or import individual categories:

```css
@import '@scilence/tokens/src/_palettes.css';
@import '@scilence/tokens/src/_spacing.css';
```

## Design Principles

- **OKLCH color space** for perceptual uniformity (creamscale excepted — uses hex to avoid green cast at high lightness)
- **Fibonacci spacing** with density multiplier for responsive compression
- **Proportional radius/borders** derived from active font size
- **Brand-hue parameterization** for white-label support: override `--brand-hue` and `--brand-hue-secondary` to shift the entire palette
