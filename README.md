# Language metadata refresh evidence

Captured by `tests/browser/tag-metadata-refresh.spec.cjs` on Linux using the pinned Playwright Chromium 145.0.7632.6.

These are mock-host component screenshots, not a complete Jellyfin session. The production pipeline, language renderer, layout and CSS run normally. The endpoint and artwork are fixtures.

- Before: two cards for the same movie show English and French audio, and an unrelated card shows Japanese.
- After receiving a tag-cache delta removing French: both movie cards show only English; the unrelated Japanese card keeps its DOM node.
- Both metadata deltas and full replacement pass on desktop/mobile Chromium. Remaining browser and gate results belong in the PR validation section.

The screenshots were visually inspected. No real media was modified and no personal server was used.
