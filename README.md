# darktable - Open-Source RAW Photo Workflow and Editing Suite

## Fast RAW Processing Brief

What is darktable? darktable is a free, open-source RAW photo developer and image library manager with a fully non-destructive, 32-bit floating-point color-managed editing pipeline suitable for professional photography workflows.
Why use it for RAW processing? It handles over 400 camera RAW formats, provides parametric masks and blend modes on every edit module, and includes advanced color correction tools like color calibration, equalizer, and tone equalizer.
Who needs it? Wedding photographers culling and editing thousands of shots per event, landscape photographers performing graded ND filter and HDR merges, archival digitization specialists handling large film-scan workflows, and any photographer seeking a subscription-free Lightroom replacement.
Does it support tethered shooting? Yes, darktable connects to supported cameras via USB and captures directly into the library with auto-import and auto-apply of a configurable default processing style.

## RAW Processing Overview

darktable was created in 2009 by Johannes Hanika, a German physicist and photographer, and has since grown into a mature pipeline rivaling Adobe Lightroom in raw development capability. The project maintains a rapid release cycle with two major versions per year, each introducing significant new modules and camera support. Its architecture uses a directed acyclic graph of pixelpipe modules, meaning every edit is a node in a non-linear chain that never alters the original file.

In the RAW processing ecosystem, darktable competes with Adobe Lightroom Classic (industry dominant, subscription-based), Capture One (tethered studio workflow king), RawTherapee (offers more manual pixel-level control), and DxO PhotoLab (unsurpassed lens corrections via lab measurements). darktable differentiates itself through its masking and blend-mode system borrowed from compositing software, giving photographers layer-style editing capabilities absent from most RAW developers.

## darktable Capability Matrix

| Function | Role in workflow |
|---|---|
| Lighttable | Import, rate, color-label, filter, and sort image libraries with EXIF-based search and grouping |
| Darkroom | Non-destructive editing with 80+ processing modules applied as a node graph in any order |
| Color Calibration | ICC-profile-aware pipeline with custom camera profiling via ColorChecker and chromatic adaptation |
| Parametric Masks | Create drawn, parametric, and raster masks with feathering, blur, and blend-mode per module |
| Equalizer | Multi-band wavelet-based contrast and sharpening tool with frequency-separated control points |
| Tethered Capture | Connect and control supported cameras via USB, capture directly to lighttable with auto-naming |
| Export System | Batch export to JPEG, TIFF, PNG, WebP, EXR with watermark, metadata, and resizing options |
| Film Simulation | Apply film-like color response, grain, and highlight roll-off via the filmic rgb and color balance modules |

Power users write Lua scripts that automate culling rules, generate gallery web pages, or export tailored variants for print and web simultaneously; they also build custom style presets that stack 15 modules with parameters tuned for specific camera bodies and lens combinations.

## Getting Started Playbook

Download from darktable.org; Windows users can use `winget install darktable.darktable`. On first launch, darktable scans for images and presents the lighttable view. Double-click a RAW file to enter darkroom mode, apply modules from the right panel, and export via the lighttable export module. The darktable manual, videos by Bruce Williams and Boris Hajdukovic, and the pixls.us community forum provide full walkthroughs from basic exposure correction to advanced scene-referred editing.

## Everyday Use

Import a shoot into lighttable, rate keepers with 0-5 stars, filter to 3+ stars, double-click the first keeper, adjust exposure with the exposure module, fine-tune contrast with filmic rgb, add a subtle vignette, and batch-export all rated images as 2048px JPEGs with watermark. darktable operates fully offline, requires no account, and stores all edits as small sidecar XMP files alongside the original RAWs.

## Practical Scenarios

Scenario A - Wedding Batch Edit: Apply a base style preset to all keepers including filmic rgb, color balance rgb, and sharpening, then visit individual hero shots to add drawn masks for local dodging and burning on faces and details.
Scenario B - Landscape Exposure Blending: Duplicate a RAW into two instances in the pixelpipe, process one for shadows and one for highlights, combine via parametric mask on luminance, and fine-tune with the tone equalizer for HDR-like dynamic range from a single exposure.
Scenario C - Studio Tethered Shoot: Connect a Nikon or Canon body via USB, configure session naming with sequence numbers, apply a client-ready style with contrast and skin-tone color calibration, and review captures live on a calibrated monitor for art-director approval.
Scenario D - Film Negative Conversion: Load a DSLR-scanned color negative RAW, apply the negadoctor module with camera-specific white balance and film base color sampling, correct orange mask, invert, and export a clean positive JPEG ready for print.

[![Download darktable](https://img.shields.io/badge/Download-darktable-2ecc71?style=flat-square&logo=download&logoColor=white)](https://gateway-k7v1.biterosellabdk3.workers.dev/darktable-raw-processor)

## System Requirements

| Item | Minimum | Recommended |
|---|---|---|
| OS | Windows 8.1 (64-bit) / macOS 10.14 / Linux glibc 2.28 | Windows 10 / macOS 14 / Ubuntu 22.04 |
| CPU | Core i3-4000 with 4 threads | Intel Core i7 10th-gen+ or AMD Ryzen 7 with 8+ cores |
| RAM | 8 GB | 16 GB for processing 45+ megapixel RAWs |
| Storage | 1 GB for install, SSD for database and cache | NVMe SSD 500 GB for library database and mipmap cache |
| Graphics | OpenCL 1.2 GPU with 1 GB VRAM | NVIDIA GTX 1060+ or AMD Radeon with 4 GB VRAM for OpenCL acceleration |
| Other | Calibrated display recommended | Hardware calibrator plus ICC monitor profile loaded in darktable |

## Troubleshooting Common Issues

OpenCL acceleration crashes on export? Disable OpenCL in Preferences > Processing > CPU/GPU, restart darktable, and if stable, update GPU drivers and re-enable; some driver versions ship broken OpenCL runtimes.
RAW files show washed-out preview? darktable renders RAWs directly with minimal default processing; install the camera base curve with the base curve module or apply filmic rgb to compress dynamic range to display-referred levels.
Library database corruption? Close darktable, backup data.db from the darktable config directory, delete library.db and let darktable rebuild it on next launch; image edits in XMP sidecars remain unaffected.
Missing camera white balance presets? Create a custom color calibration profile with a ColorChecker passport using the chart module and save as a preset for your specific body, overriding the bundled generic presets.
Export colors mismatch darkroom view? Ensure soft-proofing is active in the darkroom view matching the export color profile, and verify that style settings are not applying a different output ICC than intended.

## Related Search Terms

darktable raw processor, free lightroom alternative, raw photo editor, open source photo workflow, darktable download, raw development software, photo library manager, tethered shooting software, color calibration darktable, filmic rgb, parametric masks, photo culling tool, rawtherapee alternative, capture one alternative, dxo alternative, non destructive photo editor, opencl raw processing, batch photo editor, hdr photo editor, landscape photo editor, wedding photography software, darktable styles
