# Villa Type G153: Front Elevation, Design V2 (SketchUp)

Farah City gated community, Basra. Plot 12.50 × 20.00 m. One typical house, repeated on every plot.

V2 is a full redesign that follows the client's references: big vein-cut travertine frames, a dark bronze box frame, one strong dark balcony band with frameless glass, glowing full-height glazing and golden-hour light.

## Files

| File | What it is |
|---|---|
| `Villa_G153_Elevation.rb` | **SketchUp builder.** Run it once and it builds the full native model. Then save it as `.skp`. |
| `textures/` | Vein-cut travertine (+ `travertine_vein_n.jpg` normal/bump map for V-Ray, Enscape, D5 and Lumion), teak, curtains, bronze, paving. Keep this folder next to the `.rb` / `.dae`. |
| `Villa_G153_House.dae` | The same house as COLLADA. Use it for File ▸ Import, or in Lumion, Twinmotion, Enscape, D5 or 3ds Max. |
| `renders/` | Annotated elevation sheet, orthographic elevation, street view, three-quarter view, gated street, aerial and night. |
| `plan_check/` | Your GF / FF / roof plans as read from the DWG (1 m grid). Use them to check the model against the plan. |

## Make the .skp

1. Keep `Villa_G153_Elevation.rb` and `textures/` in the same folder.
2. Open SketchUp with a new model (template **Architectural – Meters**).
3. Open the Ruby Console: **Extensions ▸ Developer ▸ Ruby Console**, or **Window ▸ Ruby Console** in older versions.
4. Type the line below with your own path, then press Enter:
   ```ruby
   load "C:/Users/YOU/Desktop/Villa_G153/Villa_G153_Elevation.rb"
   ```
5. Use **File ▸ Save As ▸ Villa_G153_Elevation.skp**.

What the model contains:
- **One component**, `Villa G153 - Typical House`, placed 5 times along the street. If you edit one house, every house updates. For a single house, set `HOUSES_IN_STREET = 1` and `BUILD_STREET = false` at the top of the `.rb`.
- **12 tags** and named groups for every element.
- **5 scenes**: 01 Front Elevation (parallel projection), 02 Street View, 03 Three-Quarter, 04 Gated Street, 05 Aerial. Shadows are set for Basra on an October afternoon.
- **Trees and shrubs are simple placeholders** on the `09 Landscape` tag. Swap them for your 3D Warehouse, Enscape or Lumion plants. The renders use detailed trees at the same positions.

## Design V2

Left to right, as seen from the street:

1. **Travertine pier (0.80 m).** Full height on the party line, with a 40 mm dark shadow groove.
2. **Dark bronze box frame (3.24 m).** It wraps bedroom 111's floor-to-ceiling glazing and stands 1.5 m proud of the bedroom wall, set against the travertine.
3. **Travertine C-frame (6.87 m).** Its 0.80 m top band rises 0.45 m above the left block. It has a **chamfered teak soffit** that rises to the lip with an LED cove (the ref C detail). Inside are the full-height glazing of bedroom 112 and a **fluted teak wall** over the solid part of the plan wall. Its right leg sits on the plan's end pier.
4. **Side-yard slot (1.59 m).** It is finished in charcoal with a bronze screen at the GF, so it reads as a deep shadow gap between houses.
5. **One continuous 0.50 m dark bronze balcony band** with frameless glass and an LED grazer underneath. The balcony slab is deepened to 0.85 m beyond the GF wall. That is the only "simple change" to the plan, and it gives each bedroom a usable balcony, shades the GF and covers the entrance and the car.
6. **Ground floor.** Vein-cut travertine with black-framed glazing, a teak pivot door in a dark bronze portal, floating lit steps, and teak soffits with downlights over the entrance and car porch.
7. **Boundary wall (1.60 m).** Large travertine panels with dark shadow joints, a bronze grooved pedestrian gate and sliding car gate, and a travertine pier with an intercom and wall light.
8. **Roof.** A travertine stair pavilion with a thin bronze roof and teak soffit, a terrace deck, planters and a small tree.

All plan walls, openings and widths come from the DWG unchanged: W1 2.50, door 1.10, W2 1.96, W5 2.50, W6 2.20, bedroom 112 cantilever, light wells, stair room, gate openings 5.35 / 1.30 / 2.46 / 3.15 / 0.24.

## Levels (not in the DWG, so adjust to your section)

| Level | Height |
|---|---|
| Ground / sidewalk | ±0.00 |
| GF finished floor | +0.45 |
| Balcony band | +3.45 → +3.95 |
| FF finished floor | +3.95 |
| Roof finished level | +7.45 |
| Parapet / box frame top | +8.10 |
| Travertine C-frame top | +8.55 |
| Roof pavilion | +10.05 (roof plate top +10.21) |

Axes: red X runs along the street (0 = the left plot line seen from the street), green Y runs into the plot (0 = the front boundary), blue Z points up. North is +Y, so the facade faces south in the shadow settings. Change the North angle to match your site.
