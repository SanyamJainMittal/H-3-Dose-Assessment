# Tritium Dose Assessment

A multi-pathway tritium (³H) committed effective dose (CED) 
calculator based on the Public Dose Computation recommendation by AERB (India)

## Features

- **Pathway 1** — Drinking water ingestion
- **Pathway 2** — Inhalation + skin absorption
- **Pathway 3** — Food ingestion (TFWT & OBT)
  - Vegetables, Cereals, Milk, Meat, Freshwater Fish, Marine Fish
- Age-specific dose (Adult & Infant)
- Indian dietary defaults (NIN Hyderabad)
- Dose Conversion Factors from ICRP Publication 119
- Sensitivity to site-specific parameters (Ha, RH, CRs)
- Runs entirely offline — no installation required

## Methodology

Equation | Description |
|----------|-------------|
| Cam = CHTO,atm / Ha | Air moisture concentration |
| Csw = CRs × Cam | Soil water concentration |
| CTFWT = (RH×Cam + (1−RH)×Csw) / γ | Plant tissue free water tritium |
| COBT = (1−WCp) × WEQ × Rp × CTFWT | OBT in plant |
| Cafw = CRa × Cw | HTO in animal product |
| Cafw,OBT = CRa,OBT × WEQ × Rp × CTFWT | OBT in animal product |
| Cfish,HTO = WCf × Cw | HTO in fish |
| Cfish,OBT = (1−WCf) × WEQf × Rf × Cw | OBT in fish |

## Default Parameters

| Parameter | Value | Description |
|-----------|-------|-------------|
| Ha | 0.0067 kg/m³ | Absolute humidity |
| CRs | 0.23 | Soil water/air moisture ratio |
| RH | 0.73 | Relative humidity |
| γ | 0.909 | Vapour pressure ratio HTO/H₂O |
| WCp (veg) | 0.92 | Water content — vegetables |
| WCp (cereal) | 0.13 | Water content — cereals |
| WEQ | 0.51 L/kg DM | Water equivalent factor |
| Rp | 0.54 | OBT/TFWT ratio in biota |

## How to Use

### Option A — Run Online (Recommended)
Visit the live calculator:
https://sanyamjainmittal.github.io/H-3-Dose-Assessment/

### Option B — Download and Run Offline
Download index.html and open it in any browser.

## References

- Methodology for Computation of Public Dose and Apportionment based on ECPDA, AERB, India
- ICRP Publication 119 (2012). Compendium of Dose Coefficients based on ICRP Publication 60
- IAEA Safety Reports Series No. 19 (2001)

## License

MIT License — Copyright (c) 2025 Sanyam Jain, EMAD, BARC

## Developer

**Sanyam Jain**  
Environmental Monitoring & Assessment Division (EMAD)  
Bhabha Atomic Research Centre (BARC), Mumbai
