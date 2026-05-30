I used ChatGPT to architect the engineering specifications, and then fed that prompt into Claude to write the code. The prompt as follows :

Create a professional single-page engineering web application (HTML, CSS, JavaScript in one file) named:

"Microstrip Patch Antenna Design Calculator"

Purpose:
Design and visualize a rectangular inset-fed microstrip patch antenna for HFSS/CST users.

Theme:
- Dark RF engineering theme
- Responsive layout
- Print-friendly report mode
- Professional laboratory appearance

INPUTS

1. Operating Frequency f (GHz)

2. Substrate Type
   - FR4
   - Rogers RT5880
   - Custom

If FR4 selected:
εr = 4.4
h = 1.6 mm

If Rogers selected:
εr = 2.2
h = 1.575 mm

If Custom selected:
Allow manual entry of:
- Dielectric Constant εr
- Substrate Thickness h (mm)

3. Conductor Material
   - Copper
   - Silver
   - Gold
   - Aluminum
   - Custom

4. Copper Thickness t (mm)
Default:
0.035 mm
Allow custom value.

CALCULATE

Patch Width W

Patch Length L

Ground Width Wg

Ground Length Lg

Feed Width Wf

Feed Length Lf

Inset Feed Position y0

Feed Gap g

Substrate Thickness h

Copper Thickness t

Waveguide Port Width

Waveguide Port Height

Air Box Width

Air Box Height

Radiation Boundary Distance

Mesh Cell Size

Use standard rectangular microstrip patch antenna equations:

Patch Width:
W = c/(2f)*sqrt(2/(εr+1))

Effective Dielectric Constant

Fringing Length Extension

Patch Length

Ground Dimensions:
Wg = W + 6h
Lg = L + 6h

50 Ohm Feed Width

Inset Feed Position

Waveguide Port:
Port Width = 5 × Wf
Port Height = 5 × h

Air Box:
Minimum λ/4 spacing around antenna

Radiation Boundary:
λ/4

Mesh Recommendation:
Coarse = λ/20
Recommended = λ/30
Fine = λ/50

VISUALIZATION

Generate a detailed SVG engineering drawing.

Show:

- Patch
- Ground Plane
- Substrate
- Feed Line
- Inset Feed
- Waveguide Port

Display dimensions:

L
W
Lg
Wg
Wf
Lf
g
h
t
y0

Use engineering arrows and dimension lines.

Include:

1. Top View
2. Side View
3. Isometric 3D View

All dimensions should automatically update when inputs change.

OUTPUT SECTION

Display result cards for:

Patch Width W
Patch Length L
Ground Width Wg
Ground Length Lg
Feed Width Wf
Feed Length Lf
Inset Position y0
Feed Gap g
Substrate Thickness h
Copper Thickness t
Waveguide Port Width
Waveguide Port Height
Air Box Height
Air Box Width
Radiation Boundary Distance
Mesh Cell Size

PARAMETER EXPLANATION

Create a table:

Parameter | Meaning | Effect on Antenna

Explain:

f
εr
h
t
W
L
Wg
Lg
Wf
Lf
g
y0
Waveguide Port Width
Waveguide Port Height
Air Box
Radiation Boundary
Mesh Cell Size

FORMULA SECTION

Display all equations used with proper mathematical formatting.

PRINTABLE REPORT

Provide a button:

"Generate Printable Design Report"

The report must contain:

- Input Parameters
- Calculated Parameters
- Antenna Diagrams
- Formula Summary
- Design Notes
- Date & Time

HFSS/CST SECTION

Provide simulation recommendations:

- Wave Port Placement
- Radiation Boundary Placement
- Air Box Sizing
- Mesh Refinement
- Frequency Sweep Setup

The entire application must be delivered as a single self-contained HTML file with embedded CSS and JavaScript. Include comments explaining major calculation blocks and ensure all outputs update instantly when inputs change.
