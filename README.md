# PanzarUgn

A replacement front panel for a small oven, modified to fit a Novus N20K48 PID temperature controller.

## Parts

| Part | Link |
|------|------|
| Oven | https://amzn.eu/d/0dlwgoSS |
| PID controller (Novus N20K48, 48×48 mm DIN) | https://www.automation24.se/pid-temperatur-och-processregulator-novus-n20k48-820k481024 |
| Temperature sensor | _TODO: thermocouple/PT100 type_ |
| Relay / SSR | _TODO_ |

## Files

| Folder | File | Description |
|--------|------|-------------|
| `CAD/` | `panzarugn-front-panel-mod-v6.f3d` | Fusion 360 source model |
| `CAD/` | `panzarugn-front-panel-mod-v6.step` | STEP export for other CAD tools |
| `STL/` | `panzarugn-front-panel-mod-v6.stl` | **Printable front panel** (≈ 297.5 × 75 × 16 mm) |
| `STL/` | `panzarugn-front-panel-mesh-v1-aligned.stl` | Reference mesh of the original panel (for fit checking, not for printing) |
| `3DSCAN/` | `panzarugn-front-panel-scan-v1.obj` | Raw 3D scan of the original front panel |
| `3DSCAN/` | `panzarugn-side-scan-v1.obj` | Raw 3D scan of the oven side |

All dimensions are in millimetres.

## Printing

- Material: _TODO (the panel sits near a heat source; PETG or ASA/ABS recommended over PLA)_
- Layer height / infill / perimeters: _TODO_
- Supports / orientation: _TODO_

## Wiring

_TODO: describe sensor, controller and relay wiring._

> ⚠️ **Mains voltage.** This project involves wiring mains-powered heating elements. Make sure the oven is unplugged while working on it, use properly rated wire and relays, keep the protective earth connected, and get help from a qualified person if you are unsure.

## License

© Panzarkatten. This project is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0).

You may share, remix and use it commercially, as long as you give credit and share any derivatives under the same license. See [LICENSE](LICENSE) for the full text.
