# Third-party software

LightView includes PDFium 157.0.8086 for Windows x64, without V8 or XFA.

- PDFium source: https://pdfium.googlesource.com/pdfium/
- Binary distribution and NuGet package: https://github.com/bblanchon/pdfium-binaries
- NuGet: `bblanchon.PDFium.Win32` 157.0.8086, pinned in `packages.lock.json`.
- Binary release: `chromium/8086`.
- Original archive SHA-256: `1fd8af952832dbb0eb16d9249f68fe09e5f5ebf7c3dd9f6066ea2720cc28487d`.

The original archive's license and all bundled third-party notices are preserved
under `licenses/pdfium/`, including PDFium's BSD license and the licenses for
FreeType, ICU, OpenJPEG, libjpeg-turbo, libpng, HarfBuzz and other components.
The binary distribution's repository license and the Apache-2.0 license specified
by the NuGet package metadata are also included under `licenses/`.

The .NET runtime is provided by the user's system and is not included in this distribution.

## Markdown preview

- Markdig 1.4.0 (BSD-2-Clause), https://github.com/xoofx/markdig. License: `licenses/markdig/`.
- Microsoft.Web.WebView2 SDK 1.0.4129.50, https://learn.microsoft.com/microsoft-edge/webview2/. License and notices: `licenses/webview2-sdk/`. Only SDK assemblies and the x64 loader are distributed; the Evergreen Runtime is not bundled.
- Mermaid 12.1.0 (MIT), https://github.com/mermaid-js/mermaid. License: `licenses/mermaid/`.
- KaTeX 0.19.0 (MIT), https://github.com/KaTeX/KaTeX. License: `licenses/katex/`.
- DOMPurify 3.4.16 (Apache-2.0 OR MPL-2.0; used under Apache-2.0), https://github.com/cure53/DOMPurify. Licenses: `licenses/dompurify/`.
- highlight.js 11.11.1 (BSD-3-Clause), https://github.com/highlightjs/highlight.js. Browser bundle: `@highlightjs/cdn-assets` 11.11.1. License: `licenses/highlight-js/`.
- AvalonEdit 6.3.1.120 (MIT), https://github.com/icsharpcode/AvalonEdit. Text-only native viewer dependency. License: `licenses/avalonedit/`.

Mermaid's compiled bundle includes third-party components. Exact versions are
derived from its upstream source maps and listed with integrity hashes in
`licenses/markdown-dependencies/packages.json`; their notices are preserved in
the same directory and in the original bundled license comments. This includes
Mermaid's internal DOMPurify and KaTeX copies, distinct from the preview's direct
dependencies above. Browser fonts and JavaScript are included locally. No CDN,
Node.js, .NET Runtime, or WebView2 Runtime is required in the portable folder.
