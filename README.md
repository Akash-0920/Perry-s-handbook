# Refinery Unit Converter & Process Calculators

Single-file, offline-capable web app for process engineers. Perry's Handbook-style unit conversion plus quick refinery calculations. No install, no dependencies, no network calls.

## Features

### Unit converter (29 categories)
Search by category or unit (e.g. `lpm`, `psi`, `kcal`), pick From/To, get the result and a table of all units.

- Length, area, volume, mass, time
- Temperature, temperature difference (ΔT)
- Pressure (incl. kg/cm², mmHg, inH₂O)
- Volumetric flow (lpm, m³/h, gpm, bbl/d, MMscf/d…), mass flow, molar & standard gas flow (Nm³/h, Sm³/h, scfm, MMscfd)
- Density, specific volume, velocity, force
- Energy, power / heat duty (Gcal/h, MMBtu/h, TR…), specific energy, specific heat
- Heat flux, heat transfer coefficient, fouling factor, thermal conductivity
- Dynamic and kinematic viscosity, surface tension, rotational speed

### Cylinder volume
Separate unit per field (diameter, length, liquid level), vertical or horizontal, total and partial-fill volume in m³, L, US gal, bbl, ft³.

### Process calculators
| Group | Calculators |
|---|---|
| Piping & hydraulics | Line sizing (velocity, Re, ΔP, Swamee-Jain), pump head/power, NPSHa, vessel volume with 2:1 ellipsoidal / hemispherical / flat heads |
| Heat transfer & utilities | Heat duty, LMTD & area, saturated steam T↔P (approx.), heater efficiency from flue O₂ (Siegert), fuel gas MW & LHV |
| Safety | PSV fire case & API orifice selection (API 521/520), SIS PFDavg / SIL (1oo1, 1oo2, 2oo3) |
| Process | Blending (RVP index, Refutas viscosity, SG), yield / mass balance, H₂ consumption, D86 ↔ TBP (Daubert) |

## Usage

- **Online:** open `index.html` in any browser (desktop or mobile).
- **GitHub Pages:** Settings → Pages → Deploy from branch → `main` / root. Open the generated URL on your phone and use *Add to Home Screen*.
- **Offline:** download `index.html` and open it directly.

## Methods and references

- Unit factors: SI definitions, international yard/pound, US gallon, IT Btu/calorie.
- Std gas volumes: ideal gas. Nm³ = 0 °C, Sm³ = 15 °C, scf = 60 °F, all at 101.325 kPa.
- Friction factor: Swamee-Jain (turbulent), 64/Re (laminar).
- Steam: Antoine equation (two ranges) + Watson latent heat correlation, about ±1 %.
- Heater efficiency: Siegert formula, excludes radiation loss.
- PSV: API 521 fire heat input `Q = 43.2·F·A^0.82` kW (or 70.9 for poor drainage); API 520 vapour orifice equation (SI), Kc = 1.
- SIL: simplified PFDavg formulas, no CCF/β, no MTTR.
- RVP blending: RVP^1.25 index. Viscosity blending: Refutas, mass-weighted.
- D86 ↔ TBP: Daubert correlation at 760 mmHg.

## Limitations

- Pressure conversion does not apply the gauge/absolute offset.
- Line sizing is straight pipe only (no fittings).
- SUS/SSU viscosity, API gravity and ASTM D1250 volume correction are not included.
- Wetted area and fluid data for PSV sizing are user inputs.

## Disclaimer

For quick estimates and cross-checks only. Verify design, relief and SIL results with the applicable standards (API 520/521, IEC 61508/61511), licensed software and your company procedures before use. Provided as is, without warranty.

## License

MIT
