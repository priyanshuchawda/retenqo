# Website testing guide

From the repository's `web/` directory:

```bash
pnpm verify
pnpm test:e2e
pnpm audit
pnpm test:coverage
```

Unit tests live in [tests/unit](../tests/unit/) and browser tests in [tests/e2e](../tests/e2e/). They cover release metadata and validation, APK identity, synchronization failure preservation, navigation, theme switching, clipboard, download links, layout and accessibility.

Historical recorded browser execution: 98 passed, 68 skipped and 2 flaky accessibility cases passed on retry. Earlier baseline: 100 passed, 68 skipped. Full axe scans ran in Chromium desktop/mobile; Firefox and WebKit had smoke coverage. See the [complete verification record](../../docs/TESTING.md) for revision scope, formatting outcome and coverage denominators. The [engineering audit](ENGINEERING_AUDIT.md) retains the earlier baseline.

## Latest results

- Website coverage: 97.75% statements, 96.85% branches, 100% functions and 98.59% lines.
- Unit tests: 25/25 passed.
- Browser tests: 98 passed directly, 2 passed on retry, 0 skipped.
