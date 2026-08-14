# Implementation Plan: High-Fidelity Drawing Integration for index.html

The goal is to upgrade the drawing engine in `index.html` to match the professional CAD-style output of `Reactor Auto Drawing Calculator.html` (and the `drawing.png` reference), while maintaining the advanced costing and parameter inputs of `index.html`.

## Proposed Changes

### [SVG Drawing Upgrade]
- **[MODIFY] [index.html](file:///hdd2/Robinson/NodeProject/ReactorDrawing/index.html)**
    - Replace the `drawVessel()` function with a more advanced version based on the "Exact UI" logic.
    - **Layout:** Position **Top View** in the top-left and **Front View** centered.
    - **Detailing:** Add high-fidelity motor/drive symbols, pipe legs with bracing, and detailed nozzles (Inlet, Heater, Ball Valve).
    - **Labeling:** Add professional engineering callouts (Lid 2mm, 40x8 Plate, Heater 2KW, etc.) with leader lines.
    - **Dimensioning:** Implement the vertical height stack and centered internal diameter markers (`Ø`).
    - **Color Coding:** Use Black (Inner), Blue (Jacket), and Red-Dashed (Insulation) as per engineering standards.

### [Integrated CAD Tables]
- **[MODIFY] [index.html](file:///hdd2/Robinson/NodeProject/ReactorDrawing/index.html)**
    - Render a **Bill of Material (BOM)** and **Cutting Lengths** table directly inside the SVG, so they are part of the "Technical Drawing" when printed.
    - Keep the existing HTML-based cost summaries for real-time web usage, but ensure the SVG remains the "Source of Truth" for the technical sheet.

### [UI & Layout Refinement]
- **[MODIFY] [index.html](file:///hdd2/Robinson/NodeProject/ReactorDrawing/index.html)**
    - Refine the two-column layout to ensure the SVG area is large enough for the professional A3-style sheet.
    - Ensure all parameters (Clearances, Diameters, Thicknesses) are correctly linked to the new drawing engine.

## Verification Plan

### Manual Verification
- Open `index.html` and verify that the drawing area looks like a professional CAD sheet.
- Adjust parameters (e.g., `Jacket Top Clearance`) and confirm that both the Front View and the dimension stack update correctly.
- Verify that the Top View concentric circles reflect the changes in diameters.
- Perform a "Print Preview" to ensure the sheet is clean and professional for client delivery.
