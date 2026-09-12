# FileFlow Website

Bilingual static product website. The application source code is not open source.

## Edit and Preview

- Edit copy and product facts in `content/site.mjs`; the Johnny.Decimal practice guide lives in `content/johnny-decimal.mjs`.
- Edit shared page structure in `scripts/build.mjs`, styles in `site.css`, and progressive enhancements in `site.js`.
- Run `node scripts/build.mjs` to regenerate all 14 pages and `sitemap.xml`. No install step or framework is required.
- Open `index.html` or `zh/index.html` directly in a browser. Relative links also work on GitHub Pages subpaths.
- Commit generated HTML with source changes when publication is approved.

English pages retain their original URLs. Chinese counterparts live under `zh/`. Each page links to its translated counterpart, with canonical and language-alternate metadata. Both languages include the product, principles, support, privacy, terms, and first-run guide. Page content and links work without JavaScript; JavaScript adds keyboard-accessible screenshot tabs and enlargement.

## Johnny.Decimal Guide

`johnny-decimal.html` and `zh/johnny-decimal.html` explain the method through a FileFlow sample library and a manual organizing workflow. Links enter from the homepage Browse panel, step 2 of the first-run guide, and the footer. The top navigation and English-default site structure are unchanged.

The text is written for FileFlow, not copied from official documentation. It links to the [official introduction](https://johnnydecimal.com/documentation/introduction), [documentation](https://johnnydecimal.com/documentation), and [licence](https://johnnydecimal.com/support/about-legal/licence), checked September 12, 2026. The page distinguishes FileFlow's built-in starting structure, its screenshot sample library, and official Johnny.Decimal products. It makes no affiliation, endorsement, or external-index synchronization claim. Product checks used `JDDefaultData.swift`, `Config.swift`, the first-run guide, and the unchanged native captures. Publishing does not establish search indexing, rankings, AI citations, or traffic.

## Release Boundary

The 1.1 (4) app was submitted for App Review on September 12, 2026, as shown in the owner's App Store Connect submission receipt. Approval and live availability are separate facts. At the owner's request, public pages do not display temporary App Review or release-preview notices. Removing those notices is not evidence of App Store approval; the existing download link continues to point to the same App Store listing.

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

- Playwright: all 14 pages at 1440px and 390px, local image/link targets, unique headings/IDs, and horizontal overflow checks passed.
- Johnny.Decimal pages: 320/390/768/1440/1920px in both languages; text bounds, canonical/hreflang metadata, sitemap entries, all three entry routes, guide/store links, image dialogs, and no-JavaScript content passed.
- Additional 320/375/768/1920px homepage checks, hero text/image non-overlap at five sizes in both languages, gallery keyboard navigation, image dialog, FAQ, guide anchors, translated counterpart navigation, and no-JavaScript content passed.
- Selected logo and all five screenshots match their app-repository source bytes. No legacy purple icon is referenced.
- `node --check` for the builder and client script, deterministic rebuild, and `git diff --check` passed.
- Browser tests used local file URLs. These checks do not certify external link availability, mailbox delivery, or live deployment.

## Links

- Website: https://fileflow.theunclej.com (existing `CNAME`, not changed)
- Mac App Store: https://apps.apple.com/app/fileflow-file-organizer/id6756985211?mt=12
- Support: fileflow@theunclej.com (retained from existing public pages; mailbox delivery not tested)
