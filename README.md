# goiener-smartmeter-mirror
Mirror of the GoiEner smart-meter dataset (Spain, hourly household electricity, Nov 2014–Jun 2022; Universidad de Deusto / GoiEner, Zenodo v1, CC-BY 4.0) for the deviation-score (D) electricity instance.
# GoiEner smart-meter mirror (Spain, 2014–2022)

Mirror of **GoiEner smart meters data, Version 1** (Zenodo, DOI 10.5281/zenodo.7362094),
kept here so that the deviation-score (D) electricity analysis can be reproduced from a fixed copy.

- Source: https://zenodo.org/records/7362094
- Authors: Carlos Quesada Granja, Cruz Enrique Borges Hernández (Universidad de Deusto);
  Leire Astigarraga, Chris Merveille (GoiEner). Collected in the EU H2020 WHY project (GA 891943).
- Data paper: Quesada Granja et al., Scientific Data, 2024, DOI 10.1038/s41597-023-02846-0
- Licence: Zenodo record states CC-BY 4.0; the record description states CC-BY-SA.
  Files are redistributed unmodified with attribution; if CC-BY-SA applies, this mirror is
  released under the same licence.
- Coverage: ~25,000 supply points across Spain (mostly Basque Country and Navarre),
  hourly kWh, 2014-11-02 to 2022-06-08
- Downloaded: 2026-09-13. Note: Version 7 of the record became restricted on 2026-09-04;
  Version 1 remains open.

Only the raw (non-imputed) series and the metadata are mirrored. The imputed releases
(imp-pre / imp-in / imp-post, LOCF-filled) are deliberately excluded: carried-forward
values would suppress genuine consumption drops.

## Files (Release `goiener-v1`)

| File | Notes |
|---|---|
| `raw.tzst` | 2.0 GB; unpacks to ~15 GB, 25,559 CSV files (timestamp; kWh), one per anonymised supply point |
| `metadata.csv` | per supply point: contract dates, contracted_tariff (2.X households/SMEs, 3.X, 6.X), self_consumption_type, contracted power p1–p6, province, municipality (≥50k only), cnae |

MD5 as published on Zenodo: raw.tzst 6af6b9f6baddf82b7a2a663186e1e1e4; metadata.csv 1876a8fe4f0c22080e9c7936e1b0cfde.
`.tzst` = tar compressed with zstd (`zstd -d raw.tzst && tar xf raw.tar`, or 7-Zip).

## Use in the D-score project

Fourth site of the electricity instance (after London, Newcastle, Seoul Magok).
Pre-registration: OSF 9zfye — Update 2 (2026-09-13), written before any GoiEner file was downloaded.
Household selection, cohort and exclusion rules are fixed there. Analysis code lives in the
`dscore` repository; this repository holds data only.

Related mirrors: `lcl-smartmeter-mirror`, `sgsc-smartmeter-mirror`, `seoul-homeenergy-mirror`.

## Citation

Quesada Granja, C., Borges Hernández, C. E., Astigarraga, L., & Merveille, C. (2022).
GoiEner smart meters data (Version 1) [Dataset]. Zenodo. https://doi.org/10.5281/zenodo.7362094
