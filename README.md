# PanzarUgn

A replacement front panel for a small oven, modified to fit a Novus N20K48 PID temperature controller.

## Parts

| Part | Details | Purpose |
|------|---------|---------|
| Oven | [Amazon](https://amzn.eu/d/0dlwgoSS) | Base oven being modified |
| PID controller | Novus N20K48, 48×48 mm DIN panel mount — [automation24.se](https://www.automation24.se/pid-temperatur-och-processregulator-novus-n20k48-820k481024) | Temperature control |
| Temperature sensor | K-type thermocouple, 1/8" NPT EGT probe — two candidates, see [comparison](#temperature-sensor-comparison) | Measures oven temperature for the PID |
| Thermal cutoff | sourcing map KSD301, 230 °C, normally closed, 10 A / 250 V, 6.3 mm tabs, auto-reset (5-pack) — [Amazon](https://www.amazon.se/dp/B07MV7N65S) | Independent over-temperature safety cutoff |
| Power supply | MEAN WELL HDR-15-24, DIN rail, 24 V DC / 0.63 A (15.2 W) — [Amazon](https://www.amazon.se/dp/B083K1NMG3) | Low-voltage supply |
| Solid state relay | _TODO: SSR model_ | Switches the heating elements |
| SSR mounting bracket | Dioche stainless 35 mm DIN rail clamp for single-phase SSR — [Amazon](https://www.amazon.se/dp/B0BWWTH5CP) | Mounts the SSR on DIN rail |
| Push buttons | Gebildet 22 mm stainless locking push buttons, 5 A / 250 V (4-pack) — [Amazon](https://www.amazon.se/dp/B093GTW46P) | Front panel switches (control signals only, not heater current) |
| Main power switch | Heschen illuminated rocker switch, DPDT, 4 terminals, 16 A / 250 VAC, red (2-pack) — [Amazon](https://www.amazon.se/dp/B073PCDBP1) | Switches mains on/off (both poles) |

### Temperature sensor comparison

Two K-type thermocouples were bought. They appear to be the same generic probe sold under different brands; the specs differ only on paper.

| | Keenso | Tangxi |
|---|---|---|
| Link | [B07QJ9FQHP](https://www.amazon.se/dp/B07QJ9FQHP) | [B07WFZQPNK](https://www.amazon.se/dp/B07WFZQPNK) |
| Type | K, exposed tip | K, exposed tip |
| Listed range | 0–1100 °C | 0–1200 °C (description says 0–1300 °C) |
| Response time | 0.3 s | 0.3 s |
| Probe | Stainless, Ø5 mm × 80 mm | Stainless, Ø5 mm × 80 mm |
| Thread | 1/8" NPT, adjustable push-lock | 1/8" NPT, adjustable push-lock |
| Cable | 1 m | 1 m |
| Connector | Mini K-type (yellow) | Mini K-type (yellow) |
| Reviews | 3.8★ (10 ratings) — one 1★ review reports inaccurate readings and leaking seals | None |

**Which to use:** functionally either works — an oven needs well under 300 °C, far inside both ranges. Check both against a known reference (e.g. boiling water ≈ 100 °C, or a trusted oven thermometer) and keep the one that reads closest; any remaining error can be corrected with the N20K48's input offset setting. Keep the mini K connector and the cable outside the hot zone, since only the steel probe is rated for high temperature.

## Files

| Folder | File | Description |
|--------|------|-------------|
| `cad/` | `panzarugn-front-panel-mod-v6.f3d` | Fusion 360 source model |
| `cad/` | `panzarugn-front-panel-mod-v6.step` | STEP export for other CAD tools |
| `stl/` | `panzarugn-front-panel-mod-v6.stl` | **Printable front panel** (≈ 297.5 × 75 × 16 mm) |
| `stl/` | `panzarugn-front-panel-mesh-v1-aligned.stl` | Reference mesh of the original panel (for fit checking, not for printing) |
| `3dscan/` | `panzarugn-front-panel-scan-v1.obj` | Raw 3D scan of the original front panel |
| `3dscan/` | `panzarugn-side-scan-v1.obj` | Raw 3D scan of the oven side |

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
