# DART Observation Planning Tool

**DART Obs-Target-Cal** — An online tool for computing observable targets and observation windows for the Daocheng Radio Telescope (DART).

🔗 **[Open the Tool](https://Yuanao.github.io/DART_Obs-Target_Cal)**

---

## About DART

**DART (Daocheng Radio Telescope)** is a radio interferometric array based on aperture synthesis technology, completed in 2023 in Daocheng County, Sichuan Province, China. It is one of the flagship observing stations of the Chinese Meridian Project.

The array consists of **313 parabolic antennas, each 6 meters in diameter**, uniformly distributed along a circle of **1 km in diameter**. This geometry provides a nearly uniform sampling in the spatial frequency (u–v) domain with approximately 50,000 independent sampling points — making it one of the most densely sampled interferometric arrays in the world.

---

## Key Specifications

| Parameter | Value |
|-----------|-------|
| Number of antennas | 313 × 6 m parabolic dishes |
| Array diameter | 1 km |
| Frequency range | 149 – 459 MHz |
| Simultaneous channels | 2 (each up to 4 MHz bandwidth) |
| Channel bandwidth options | 125 kHz / 1 MHz / 2 MHz / 4 MHz |
| Angular resolution (450 MHz) | ~100 arcsec |
| Field of view (150 MHz) | up to 20° × 20° |
| Field of view (450 MHz, 3 dB) | ~2° × 2° |
| Time resolution (standard) | 100 – 500 ms |
| Time resolution (fast mode) | 5 ms |
| Amplitude calibration accuracy | 0.2 dB (~±2.3%) |
| Phase calibration accuracy | 2.5° |
| Polarization measurement error | < 5% |
| Minimum observable elevation | 15° |

---

## Observing Modes

**Dual-frequency tracking mode** — Two simultaneous center frequencies within 149–459 MHz (separation ≤ 40 MHz), integration time 5–1000 ms. Used for standard radio source imaging.

**Single-frequency scanning mode** — Steps through center frequencies sequentially to achieve broadband coverage across the full 150 MHz band. Each frequency produces images with different FoV and angular resolution.

---

## Polarization

DART simultaneously records dual-polarization (HH, VV) and cross-polarization (HV) visibilities. After calibration, the four Stokes parameters are derived as:

```
I = (S_HH + S_VV) / 2
Q = (S_HH - S_VV) / 2
U = Re(S_HV)
V = −Im(S_HV)
```

---
## This Planning Tool

| Mode | Description |
|------|-------------|
| **Free Target** | Input any RA/Dec (any format) and date → compute rise, transit, set times and elevation |
| **Globular Clusters** | Computes observable GCs (Harris 1996 catalog) for a given date |
| **SNR** | Computes observable supernova remnants (Green 2019 catalog) for a given date |
| **Galactic Survey** | Generates full-sky transit time and peak elevation maps for the Galactic plane |

All times are in **Beijing Time (BJT = UTC+8)**. Observation window: 18:00 BJT to 08:00 BJT next day.

---

*Star catalogs: Harris 1996 rev. 2010 (Globular Clusters) · Green 2019 (SNR) · Galactic coordinate conversion based on IAU 1958*  
*Calculation method: spherical astronomy approximation, accuracy ±2 min*
