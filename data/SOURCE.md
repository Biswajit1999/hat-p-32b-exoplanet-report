# Data sources

## TESS light curve

- File: `tess2022302161335-s0058-0000000292152376-0247-s_lc.fits`
- Archive: Mikulski Archive for Space Telescopes (MAST), TESS SPOC light-curve product
- TESS sector: 58
- TIC target ID: 292152376
- MAST observation ID: 104654331
- MAST data URI: `mast:TESS/product/tess2022302161335-s0058-0000000292152376-0247-s_lc.fits`
- Exact download URL: <https://mast.stsci.edu/api/v0.1/Download/file?uri=mast:TESS%2Fproduct%2Ftess2022302161335-s0058-0000000292152376-0247-s_lc.fits>
- Collection DOI: [10.17909/t9-nmc8-f686](https://doi.org/10.17909/t9-nmc8-f686) (TESS 2-minute light curves, all sectors; sector 58 used here)
- Retrieved: 2026-08-15
- SHA-256: `808d5c6fa9608095cc7638e91424fefac5232af2c2b0df3ee5b4766c6f5ebc69`

The FITS file is stored unmodified. The analysis reads `TIME`, `PDCSAP_FLUX`,
`PDCSAP_FLUX_ERR`, and `QUALITY`. PDCSAP flux is the SPOC light curve with common
instrumental trends removed and aperture/crowding corrections applied; this does
not make it free of residual stellar or instrumental systematics.

## System parameters

- File: `system_parameters.csv`
- Service: NASA Exoplanet Archive TAP, `pscomppars` table
- Exact query: <https://exoplanetarchive.ipac.caltech.edu/TAP/sync?query=select+pl_name%2Chostname%2Cra%2Cdec%2Cpl_orbper%2Cpl_tranmid%2Cpl_trandur%2Cpl_rade%2Cpl_bmasse%2Cpl_eqt%2Cpl_orbsmax%2Csy_dist%2Csy_tmag%2Cst_teff%2Cst_rad%2Cst_mass%2Cdisc_year%2Cdiscoverymethod%2Cdisc_refname%2Cdisc_pubdate%2Cdisc_facility+from+pscomppars+where+pl_name%3D%27HAT-P-32+b%27&format=csv>
- Retrieved: 2026-08-15

The saved row is the input actually used by `scripts/analyze_transit.py`; the
analysis does not query a changing live service at run time.


## Additional TESS sectors for robustness analysis

All are unmodified standard-cadence SPOC light curves from the same [MAST TESS collection](https://doi.org/10.17909/t9-nmc8-f686).

- Sector 58: `tess2022302161335-s0058-0000000292152376-0247-s_lc.fits` (2,027,520 bytes)
  - MAST URI: `mast:TESS/product/tess2022302161335-s0058-0000000292152376-0247-s_lc.fits`
  - SHA-256: `808d5c6fa9608095cc7638e91424fefac5232af2c2b0df3ee5b4766c6f5ebc69`
