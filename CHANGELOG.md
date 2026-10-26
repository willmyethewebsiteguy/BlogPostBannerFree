# Changelog

## 3.1.6 — 2026-10-26

- Fix initialization on Squarespace's component-based blog sections while retaining legacy section selectors.
- Correct banner background positioning and duplicate-title visibility.
- Preserve article title alignment, metadata visibility, content width, and background color.
- Handle missing post data, image URLs, and focal points; recognize the newer edit-mode class.

Existing installs using `@3.1` receive this patch after CDN cache refresh. No code injection change is required. Exact-version installs must update to `@3.1.6`.

Pinned script:
`https://cdn.jsdelivr.net/gh/willmyethewebsiteguy/BlogPostBannerFree@3.1.6/blogbanner-javascript.min.js`

The repository contains source JavaScript and CSS; jsDelivr generates the `.min.js` and `.min.css` variants automatically.

Validation: original CDN script reproduced a null-section error on https://www.will-myers.com/blog-styles/style-1. Patched free script and CSS were injected in place of the paid assets in a test browser; banner/image rendering, original-title hiding, author visibility, and absence of horizontal overflow were checked at 1440px and 500px. Live Squarespace 7.0 regression testing was not performed.
