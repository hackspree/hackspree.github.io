# Website Specifications

## User-facing behavior

- The site is a single-page personal landing page served from `index.html`.
- The page shows the Hackspree logo on the left on wide screens and above the content on narrow screens.
- The main content presents Mohamed A. Fouad's name, a short engineering-focused tagline, a quote, and a row of social/profile links.
- The social/profile row includes links for GitHub, X, LinkedIn, Discord, the MSc thesis, and the Hackspree blog at `https://blog.hackspree.com`.
- Social/profile links open in a new tab and expose accessible `aria-label` text.
- Each social/profile icon shows a custom hover hint with link-specific copy after a short intentional hover delay.
- The Hackspree logo is intentionally displayed slightly smaller than the earlier oversized presentation, targeting roughly a 10-15% size reduction on both desktop and mobile layouts.

## Implementation rules

- `index.html` is the source of truth for layout, content, and styling.
- Font Awesome icons are loaded from the existing CDN stylesheet and should be reused for social/profile links.
- The blog link should use a Font Awesome icon consistent with the rest of the social/profile icon row.
- Social/profile hover hints should be implemented in CSS using per-link metadata on the anchor so the delay and styling are consistent across icons.
- Responsive behavior is controlled with the existing CSS media query at `max-width: 900px`.

## Constraints and invariants

- Preserve the current black background, dark aesthetic, and Orbitron typography.
- Preserve the existing two-column desktop layout and stacked mobile layout.
- Preserve external link safety attributes for outbound links (`target="_blank"` with `rel="noopener noreferrer"`).
- Keep the social/profile row keyboard-accessible, with hover-hint behavior also available on visible focus.
