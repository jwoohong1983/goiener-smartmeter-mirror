# GoiEner smart-meter data (mirror)

Unmodified mirror of the GoiEner smart-meter dataset, retained with attribution as the Creative
Commons Attribution 4.0 licence permits, for the pre-registered analysis at https://osf.io/9zfye.

## Source

Quesada Granja, C., Borges Hernández, C. E., Astigarraga, L., & Merveille, C. (2022).
*GoiEner smart meters data* (Version 1) [Dataset]. Zenodo.
https://doi.org/10.5281/zenodo.7362094

Authors: Carlos Quesada Granja, Cruz Enrique Borges Hernández (Universidad de Deusto);
Leire Astigarraga, Chris Merveille (GoiEner).

Licence: Creative Commons Attribution 4.0. Coverage: about 25,000 supply points, mostly in the
Basque Country and Navarre, hourly kWh, 2014-11-02 to 2022-06-08.

Files here are byte-identical copies of the Zenodo release. Prefer Zenodo as the citable source;
this mirror exists so that the analysis inputs remain retrievable at a fixed address.

## What the analysis uses

The **raw, non-imputed** series only. The imputed releases are filled by last observation carried
forward, which would suppress exactly the downward movements this study measures.

| File | Bytes | Integrity |
|---|---|---|
| `metadata.csv` | 5,579,767 | SHA-256 `dcb3792e6967317221976cc78ac02d15dd9463020f81aa5b97dd081235e88387` |
| `raw.tzst` | — | Verify against the MD5 published alongside the file on Zenodo |

Exclusions applied per the pre-registered specification: self-consumption supply points, and
non-residential points identified by contracted tariff and CNAE code. 25,559 supply points reduce to
20,509 after exclusions.

## Related

- London panel: `lcl-smartmeter-mirror` — provenance only, no data hosted
- Australian panel (Smart Grid Smart City): `sgsc-smartmeter-mirror`
- Korean reference panel: `seoul-homeenergy-mirror` — provenance only, no data hosted
- Full source record for all four panels: `DATA_SOURCES.md` in the analysis repository

Mirrored by Jung Woo Hong (2026-09) for the pre-registered analysis at https://osf.io/9zfye.

## Citation

Quesada Granja, C., Borges Hernández, C. E., Astigarraga, L., & Merveille, C. (2022).
GoiEner smart meters data (Version 1) [Dataset]. Zenodo. https://doi.org/10.5281/zenodo.7362094
