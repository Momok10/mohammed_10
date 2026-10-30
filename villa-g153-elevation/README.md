# Villa Type G153: Designed Front Elevation (SketchUp)

Farah City gated community, Basra. Plot 12.50 × 20.00 m. One typical house, repeated on every plot.

## Files

| File | What it is |
|---|---|
| `Villa_G153_Elevation.rb` | **SketchUp builder.** Run it once and it builds the full native SketchUp model. Then save it as `.skp`. |
| `textures/` | Travertine, teak, bronze seam, paving, grass and foliage textures. Keep this folder next to the `.rb` / `.dae`. |
| `Villa_G153_House.dae` | The same house as COLLADA. Use it as a fallback (File ▸ Import) or in Lumion, Twinmotion, Enscape, D5 or 3ds Max. |
| `renders/` | Annotated elevation sheet, orthographic elevation, perspectives, gated-street view, aerial and night view. |
| `plan_check/` | Your GF / FF / roof plans as read from the DWG, with a 1 m grid. Use these to check that the model follows the plan. |

## Make the .skp (about 1 minute)

1. Unzip and keep `Villa_G153_Elevation.rb` and `textures/` in the same folder.
2. Open SketchUp with a new model (template **Architectural – Meters**).
3. Open the Ruby Console: **Extensions ▸ Developer ▸ Ruby Console** (SketchUp 2021+), or **Window ▸ Ruby Console** in older versions.
4. Type the line below with your own path, then press Enter:
   ```ruby
   load "C:/Users/YOU/Desktop/Villa_G153/Villa_G153_Elevation.rb"
   ```
5. When the console prints `Villa G153 built ...`, use **File ▸ Save As ▸ Villa_G153_Elevation.skp**.

What you get in SketchUp:
- **One component**, `Villa G153 - Typical House`. Five instances stand side by side on 12.50 m plots along a street. If you edit one house, every house in the street updates.
- **12 tags**: massing, travertine, bronze, glazing, timber, balcony, roof pavilion, boundary wall, landscape, lighting, curtains, site. Each element is a named group (see the Outliner).
- **5 scenes**: 01 Front Elevation (parallel projection), 02 Street Perspective, 03 Entrance Close-up, 04 Gated Street, 05 Aerial. Shadows are set for Basra (30.5° N) on an October afternoon.
- For a single house without the street, edit the top of the `.rb`: `HOUSES_IN_STREET = 1` and `BUILD_STREET = false`.

## Plan fidelity

Every wall line was measured from the DWG: the ground floor plan, the first floor plan and the roof plan.

- **Plan form and exterior walls are unchanged.** That covers the guest-room front (W1 2.50 m, door 1.10 m), the WC set-back, the hall (W2 1.96 m), the side-yard slot, the bedroom 111 / 112 faces (W5 2.50 m, W6 2.20 m), the 1.84 m bedroom 112 cantilever over the car porch, the 7.88 m balcony, the roof canopy line, the light wells, the stair room and the boundary openings (5.35 / gate 1.30 / 2.46 / car gate 3.15 / 0.24).
- **Added elements only:** facade cladding layers, the travertine frame legs, bronze lining, the balcony glass, the pergola, the entrance canopy, the screens, the roof canopy, planters and landscape.

## Design concept

1. **Two-storey travertine frame.** It wraps the FF loggia and stands 0.57 m in front of the balcony edge. Its full-height left leg is the hero gesture, and it gives deep shade to the bedrooms.
2. **Dark bronze band.** The balcony edge slides *through* the frame and carries on as the car-porch pergola. This one horizontal line ties the whole frontage together, and an LED grazer is set under it.
3. **Floating bronze box.** The cantilevered bedroom 112 is clad in standing seam with a vertical light slot. The pergola planter sits in front of it.
4. **Warm inner layer.** Fluted teak walls, a teak soffit with downlights, floor-to-ceiling bronze-framed sliding glazing with sheer curtains, and a frameless glass balustrade.
5. **Ground floor.** The guest window has a bronze box frame with angled teak fins (privacy and sun control). There is a teak pivot door in a bronze portal with a canopy, and floating lit steps.
6. **Street edge.** A travertine boundary wall in 1.26 m panels with shadow joints, a planter on the street side, slatted bronze gates, a backlit house number and date palms on the plot lines.
7. **Roof.** A stair pavilion with a floating canopy (teak soffit), a terrace deck and planters whose greenery shows above the parapet.

## Levels used (not in the DWG, so adjust to your section)

| Level | Height |
|---|---|
| Ground / sidewalk | ±0.00 |
| GF finished floor | +0.45 |
| FF finished floor | +3.95 (floor-to-floor 3.50) |
| Roof finished level | +7.45 |
| Frame / parapet top | +8.45 |
| Roof pavilion / canopy top | +10.20 / +10.45 |

Model axes: red X runs along the street (0 = the left plot line seen from the street), green Y runs into the plot (0 = the front boundary), blue Z points up. North is +Y, so the facade faces south in the shadow settings. Change the North angle if your site faces another way.
