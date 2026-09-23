# Rayglass Support

For Rayglass on Mac and Rayglass Mobile.

Rayglass provides local optical modeling, ray tracing, and analysis. Start from an example, edit a prescription, compare results, and save your project or export plots and data.

## Contact

Developer / operator: Dongsheng Hu
Support email: hudongsheng356@gmail.com

When reporting an issue, include the app version, operating system, device model, steps to reproduce, and expected and actual results. If helpful, attach a screenshot or minimal example project with sensitive information removed. Do not send passwords, payment details, or confidential designs you are not authorized to share.

## Requirements

- Mac: macOS 14 or later.
- iPad: iPadOS 17 or later.
- Core calculations work offline. No account or external optical hardware is required. Opening external material-source pages requires internet access.

## Language

Rayglass supports English and Simplified Chinese. It follows the app language selected in your system settings; reopen the app after changing it. Unmatched languages fall back to English. Existing project titles, surface names, and notes retain their original text. Newly created built-in examples use the current language.

## Your First Design

1. Open Elements & Examples and load the N-BK7 / N-F2 doublet.
2. Open Optical Design. On Mac, edit the table and inspector. On iPad, tap a surface card to open its parameter sheet.
3. Adjust radius, spacing, or aperture and wait for tracing to finish.
4. Select Auto Focus, then open Spot Analysis to inspect RMS, fields, and wavelengths.
5. Use Save Project or Save Project As to save a .rayglass file.

Lengths are generally in mm, wavelengths in µm, and angles in degrees. Coating thickness is in µm. A radius of 0 denotes a plane. Always check the unit shown beside the input.

## Materials and Elements

Search Materials and apply a glass to the selected refractive surface. On iPad, expand the material first. The 156 SCHOTT entries are a historical snapshot with sources and wavelength ranges; they do not represent live availability, melt data, or thermal data. Select a surface followed by air before inserting a separate optical element.

## Saving and Exchanging Projects

.rayglass files save the optical prescription, system settings, and supported coating and non-sequential parameters. Surface CSV files contain only part of the prescription and do not replace a project file. Optimization variables, tolerance recipes, and complete analysis histories are not all saved; configure those runs again after reopening a project.

On Mac, open or save from the toolbar or File menu. On iPad, use Open Project or Save Project As in the top-right ellipsis menu. Transfer files manually through a location you choose, including cloud locations provided by the system. Rayglass does not provide automatic cross-device synchronization. Older versions may discard newer fields when saving; keep a backup before exchanging files between versions.

Recovery copies help reduce the impact of interruptions but do not replace independent backups. Removing the app, clearing its container, or device failure can cause a recovery copy to be lost.

## Exporting Results

Export ray-layout PNG images, Markdown analysis reports, surface CSV files, and CSV data offered by individual analysis pages. On Mac, use Exchange and the module export buttons. On iPad, use the ellipsis menu and module export buttons. Some exports require running the corresponding analysis first.

## Frequently Asked Questions

### Why is ray throughput below 100%?

Rays may be clipped, undergo total internal reflection, or fail to reach a valid intersection. Check apertures, materials, surface order, spacing, and diagnostics. Sequential throughput is a fraction of sampled rays, not transmitted optical power.

### Why will diffraction analysis not run?

The current model requires a centered system, an infinite object, an on-axis field, no mirrors, air exit, no clipping, and NA ≤ 0.1. Check decenter, tilt, media, and sampling. Compare results at higher sampling to assess convergence.

### Why does an iPad analysis page extend beyond the window?

Complex pages scroll horizontally. Use landscape or a wider window to see more controls at once. Content also scrolls vertically.

### What if a calculation takes too long?

Reduce sampling or the number of tolerance trials and start with a smaller run. Select Stop to cancel. On iPad, entering the background cancels the current calculation and preserves a recovery copy.

### Can I use Zemax files, CAD, or Python scripts?

ZMX/ZOS projects, general CAD import, and in-app script execution are not supported. Use .rayglass and CSV for supported file exchange.

### Are the Mac and iPad versions identical?

They share the same origin for their calculation models, with interfaces adapted to each platform. The iPad Materials page does not currently include Mac's multi-material comparison, catalog scatter plot, or filtered catalog CSV export. Versions are released independently; consider version differences when exchanging files.

## Model Limits

Sequential analysis does not perform pupil aiming at arbitrary internal stops. Diffraction uses a restricted paraxial scalar model. Optimization is bounded local search, not a guarantee of a global optimum. Tolerance perturbations are independent and uniform. Basic non-sequential analysis excludes general CAD, scattering, and nested media. Coatings use an independent lossless dielectric model and are not coupled to surface tracing. Manufacturing and consequential engineering decisions require independent benchmarks and measurements.
