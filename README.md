# FileFlow Website

Bilingual static product website. The application source code is not open source.

## Edit and Preview

- Edit copy and product facts in `content/site.mjs`.
- Edit shared page structure in `scripts/build.mjs`, styles in `site.css`, and progressive enhancements in `site.js`.
- Run `node scripts/build.mjs` to regenerate all 12 pages and `sitemap.xml`. No install step or framework is required.
- Open `index.html` or `zh/index.html` directly in a browser. Relative links also work on GitHub Pages subpaths.
- Commit generated HTML with source changes when publication is approved.

English pages retain their original URLs. Chinese counterparts live under `zh/`. Each page links to its translated counterpart, with canonical and language-alternate metadata. Both languages include the product, principles, support, privacy, terms, and first-run guide. Page content and links work without JavaScript; JavaScript adds keyboard-accessible screenshot tabs and enlargement.

## Release Boundary

The 1.1 (4) app was submitted for App Review on September 12, 2026, as shown in the owner's App Store Connect submission receipt. Approval and live availability are not yet verified. `site.release.status` is therefore `in-review`: the website labels 1.1 screenshots as a preview and distinguishes them from the latest approved App Store version. Change this only after verifying actual availability, then rebuild.

The owner authorized committing and pushing this website revision on September 12, 2026. GitHub Pages is configured to publish from the root of `main`; check the Pages deployment result for publication status. Website publication does not imply App Store approval. Existing copyright holder/year and the main site's support address are preserved. Prices are not hardcoded. Privacy and terms copy is aligned with the product's data flows and recovery limits; this is not a legal certification.

## Source Alignment

- Current UI: five unmodified native captures from `FileFlow/planning/design/assets/app-store-1.1-build-4/native/en/`, using fictitious sample files and the uploaded 1.1 (4) archive. Both site languages currently show the English app UI. Old screenshots are retained but unreferenced.
- App icon: `AppIconOriginalFlowOrange.appiconset/icon_256x256@2x.png`, verified against the current Xcode build setting. This is the selected original-flow orange derivative, not the legacy purple `AppIcon` catalog. The original source is preserved.
- First-run guide: adapted from `FileFlow/docs/website-first-run-tutorial.zh-CN.md` (September 11), updated to start with the manual Inbox path rather than requiring AI.
- Manual flow, AI request data, and recovery: current `ASC_RELEASE_20260912_DRAFT.md` source anchors, Inbox/Review plan source, `LLMPromptBuilder`, and `UndoService`.
- Quota: current `Utilities/FeatureGate.swift` defines 50 lifetime file operations; Pro removes that quota. Local prices remain on the App Store and purchase sheet.
- Storage and diagnostics: `FileflowConfigurationStore`, `RootRecoveryReceiptService`, `APIKeyService`, and the disabled configured state in `CrashReportingService`.

Do not restore blanket promises of universal Undo, exclusively local AI processing, or all app data living inside the selected root. Do not treat a stored receipt or index as a file backup.

## Local Verification (September 12, 2026)

- Playwright: all 12 pages at 1440px and 390px, local image/link targets, unique headings/IDs, and horizontal overflow checks passed.
- Additional 320/375/768/1920px homepage checks, hero text/image non-overlap at five sizes in both languages, gallery keyboard navigation, image dialog, FAQ, guide anchors, translated counterpart navigation, and no-JavaScript content passed.
- Selected logo and all five screenshots match their app-repository source bytes. No legacy purple icon is referenced.
- `node --check` for the builder and client script, deterministic rebuild, and `git diff --check` passed.
- Browser tests used local file URLs. These checks do not certify external link availability, mailbox delivery, or live deployment.

## Links

- Website: https://fileflow.theunclej.com (existing `CNAME`, not changed)
- Mac App Store: https://apps.apple.com/app/fileflow-file-organizer/id6756985211?mt=12
- Support: fileflow@theunclej.com (retained from existing public pages; mailbox delivery not tested)
