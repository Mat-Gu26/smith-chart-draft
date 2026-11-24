# Smith Chart Drafting Studio

A precision, browser-based **compass-and-straightedge drafting studio** for the Complete Smith Chart. Built for RF, microwave, and transmission-line work where you want to draw exact centered circles, radial rays, circular rotation arrows, and ruler drop lines visually—with optional exact RF math input whenever you need multi-decimal accuracy.

### [Launch Live App](https://<your-username>.github.io/<repo-name>/)

<!-- Optional: Once you add screenshot.png to your repo, uncomment the line below -->
<!-- ![Smith Chart Drafting Studio Preview](screenshot.png) -->

---

## Why This Exists

Most online Smith Chart tools work like black-box calculators where you type in component values and watch plots appear. When learning or solving transmission-line problems by hand (or documenting graphical constructions for homework and reports), you often want a **true digital compass and straightedge**:

- Circles strictly locked to the exact chart center (`$z = 1 + j0$`)
- Straight radii and diameters locked through the exact center out to the wavelength/angle rings
- Circular rotation arrows showing `$\Delta\lambda$` clockwise (WTG) or counter-clockwise (WTL)
- Vertical drop lines straight down to the bottom Radially Scaled Parameters rulers
- Optional exact math editing when cursor precision isn't quite enough (e.g., placing a point at exact `$z = 0.473 - j1.351$`)

---

## Key Features

### Publication-Grade Vector Complete Smith Chart
- Mathematically exact constant-resistance (`$r$`) circles and constant-reactance (`$\pm jx$`) arcs with clean visual density clipping and crisp `$\infty$` symbols.
- All four concentric outer scale rings:
  1. Angle of Transmission Coefficient (degrees)
  2. Angle of Reflection Coefficient (degrees)
  3. Wavelengths Toward Load (WTL, `$\lambda$`)
  4. Wavelengths Toward Generator (WTG, `$\lambda$`)
- Aligned **Radially Scaled Parameters** bar (SWR, dBS, Return Loss, Reflection Coefficient `$P$` and `$E/I$`, Attenuation, Transmission Coefficient, Origin rail) with a live **Divider Scale Projection** overlay.

### Locked Compass & Straightedge Tools
- **Centered Circle (`C`):** Always locked to `$z = 1 + j0$` for constant-VSWR circles.
- **Radius (`R`) & Diameter (`D`):** Locked through the exact center, toggleable to extend across the outer wavelength/angle scales or stop at the `$|\Gamma| = 1$` rim.
- **Circular Arrow (`A`):** Centered rotation arcs with smart snapping onto existing radii, circles, points, or intersections. Supports Auto/CW/CCW sweep, single or double-ended arrowheads, quick direction flip (`F`), and automatic `$\Delta\lambda$` labels.
- **Vertical Drop Line to Rulers (`U`):** Snaps the top anchor to any plotted element or free point and drops vertically down through the bottom Radially Scaled Parameters with live ruler readings.
- **Point Marker (`P`) & Free Straight Line (`L`):** Drop labeled markers (`zL`, `yL`, `P1`, etc.) or connect any two points.
- **Full Styling Controls:** 8 high-contrast drafting colors + custom color picker, solid/dashed/dotted strokes, 3 stroke widths, and collapsible Elements/Layers manager.

### Precision Snapping & Exact Math Editor
- **Magnetic Snapping:** Automatically snaps to intersections (circle-ray, circle-line, ray-rim, drop-line intersections), points, radii/diameters, circles, and the `$|\Gamma| = 1$` rim.
- **Create & Edit by Math Expression:** Select any element (or use **Create by Math Expression**) to set exact coordinates using flexible RF notation:
  - Normalized impedance `$z = r \pm jx$` (e.g., `0.473 - j1.351`, `-j0.8`, `2.5`)
  - Normalized admittance `$y = g \pm jb$`
  - Reflection coefficient `$|\Gamma|$` and `$\angle\Gamma$` (degrees)
  - VSWR, Return Loss (`$\text{dB}$`), WTG (`$\lambda$`), WTL (`$\lambda$`), or sweep `$\Delta\lambda$`
- **Live Readout HUD:** Tracks `$\angle\Gamma$` (degrees), WTG (`$\lambda$`), WTL (`$\lambda$`), `$z$`, `$|\Gamma|$`, and VSWR smoothly inside the chart and across the outer rings—and can be hidden anytime for pure paper-and-compass practice.

### Import & High-Resolution Export
- **Import Custom Charts (PDF / SVG / PNG / JPG):** Load your own preferred Smith Chart with automatic missing-`$\infty$` glyph repair for SVGs and a 2-click Center & Rim calibration.
- **Export:** Download your completed construction as a crisp **3200px PNG** or a standalone **vector SVG**.

---

## Keyboard Shortcuts

| Key | Action |
| :--- | :--- |
| `C` | Centered Circle tool |
| `R` | Radius Line tool |
| `D` | Diameter Line tool |
| `A` | Circular Arrow (Arc Arrow) tool |
| `U` | Vertical Drop Line to Rulers tool |
| `P` | Point Marker tool |
| `L` | Free Straight Line tool |
| `V` | Select / Edit tool |
| `H` or hold `Space` | Pan canvas |
| `Scroll Wheel` | Zoom in / out at cursor (up to `$10\times$`) |
| `F` | Flip Circular Arrow direction (CW / CCW) |
| `]` | Collapse / expand right Inspector & Elements panel |
| `Ctrl+Z` / `Ctrl+Y` | Undo / Redo |
| `Delete` / `Backspace` | Delete selected element |
| `Esc` | Cancel current drawing or deselect |

---

## Running Locally

This entire app lives in a single self-contained `index.html` file with no build step and no backend:

1. Download `index.html` from this repository.
2. Double-click `index.html` to open it in any modern desktop or mobile browser.

---

## Privacy

- **100% client-side:** All drawing, math calculations, custom PDF/SVG imports, and PNG/SVG exports happen locally inside your browser.
- No accounts, no tracking, no analytics, and no files are ever uploaded to a server.

---

## Feedback & Roadmap

Suggestions, bug reports, and feature requests from students, professors, and RF engineers are very welcome! Feel free to open an **Issue** with ideas. Potential upcoming additions under consideration:

- Lossy transmission-line spiral arrows & attenuation (`$\text{dB}$` / `$\text{Np}$`) shift
- Toggleable Admittance (`$Y$`) grid overlay (`$ZY$` chart mode)
- Constant-`$r$` / constant-`$g$` matching network arcs (series & shunt `$L/C$` and stubs)
- Off-center & rotated `$g = 1$` circles (double-stub matching, stability/gain circles)
- Save & reload project files (`.json`)

---

## License

Released under the [MIT License](LICENSE).