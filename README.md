# Mars HexaLogic: Comparative Planetary Analog Analysis & Telemetry Interface

**Mars HexaLogic** is a client-side scientific visualization and comparative planetary science platform developed by **Team HexaLogic** (Marwa, Marwan, and Rahma). The system establishes an empirical framework for evaluating terrestrial extreme environments (**Mars Analog Sites**) against their morphological and climatological counterparts on Mars, utilizing authenticated datasets from NASA archives.

**Live Deployment:** [https://marwa95ae.github.io/Mars/](https://marwa95ae.github.io/Mars/)

---

## 1. Scientific Rationale & Methodology

Terrestrial analog research is fundamental to planetary exploration, enabling the calibration of remote-sensing instruments, validation of climate models, and testing of In-Situ Resource Utilization (ISRU) protocols prior to deep-space deployment. 

This platform conducts a multi-parametric comparative analysis across **five primary geophysical and meteorological vectors**:
1. **Surface & Near-Surface Temperature ($T_s$)**
2. **Atmospheric Surface Pressure ($P_s$)**
3. **Geomorphology & Regolith Composition**
4. **Incident Solar Irradiance ($S$)**
5. **Aeolian Dynamics & Wind Velocity ($v_w$)**

### Comparative Matrix of Target Sites

| Terrestrial Analog Site | Martian Counterpart | Primary Comparative Basis |
| :--- | :--- | :--- |
| **McMurdo Dry Valleys** (Antarctica) | **Martian South Polar Region** | Hyper-arid, cryotic polar desert conditions; sublimation-dominated hydrology and ice-cemented permafrost. |
| **Atacama Desert** (Yungay Core, Chile) | **Noctis Labyrinthus** | Extreme non-polar hyper-aridity, high UV flux, sulfate/perchlorate-rich regolith, and minimal biological activity. |
| **Haughton Impact Crater** (Devon Island, Canada) | **Gale Crater** | High-latitude impact structure exhibiting preserved paleolacustrine deposits, hydrothermal alteration, and periglacial weathering. |

---

## 2. System Architecture & Analytical Modules

The application is engineered as a zero-dependency **Single-Page Application (SPA)** to ensure deterministic performance, low latency, and offline-capable data inspection.

* **Synchronized Dual-Planet Geospatial Engine:** Integrates high-resolution orbital imagery from **Esri World Imagery** (Earth) alongside **NASA Mars Trek Web Map Tile Service (WMTS)** layers (Mars) for direct side-by-side geomorphological inspection.
* **Longitudinal Time-Series Visualization (SVG Sparklines):** Renders vectorized telemetry trends comprising **60 monthly terrestrial observations (2020–2024)** derived from satellite reanalysis and **133 seasonal Martian data points** across a full Martian solar longitude ($L_s$) cycle.
* **Mars24 Chronometry & Mission Control Module:** Computes real-time **Martian Sol** count and **Local Mean Solar Time (LMST)** at the *Perseverance* rover landing site (Jezero Crater) by converting Coordinated Universal Time (UTC) to Terrestrial Time (TT) and Julian Date ($JD_{TT}$), accounting for the synodic Martian solar day ($88,775.244\text{ seconds}$).
* **Parametric Life-Support & Habitat Calculators:** Deterministic models estimating oxygen, potable water, and power requirements based on crew size and mission duration constraints.
* **Stratified Presentation Modes (`Explorer` vs. `Researcher`):** Dynamically toggles DOM visibility states between conceptual summaries for public outreach (`Explorer`) and raw SI units, physical constants, and analytical equations for domain specialists (`Researcher`).

---

## 3. Data Provenance & NASA Source Register

To maintain scientific rigor and traceability, all empirical values and environmental parameters are indexed via inline citations `[n]` mapped to an integrated **NASA Source Register**:

* **Terrestrial Climatology:** Sourced from the **NASA Prediction Of Worldwide Energy Resources (POWER)** project (MERRA-2 assimilation model).
* **Martian Atmospheric Modeling:** Derived from the **NASA Ames Mars Global Climate Model (MGCM)** outputs and **Mars Climate Database (MCD)** seasonal profiles.
* **Planetary Cartography & In-Situ Telemetry:** Referenced against the **NASA Planetary Data System (PDS)** and **Mars Trek** geospatial repositories.

---

## 4. Technical Implementation

* **Core Stack:** Semantic HTML5, CSS3 (Custom Keyframe Animations, CSS Custom Properties, Responsive Grid Architecture), Vanilla ECMAScript (ES6+ State Management & Hash/Slide Routing).
* **Data Representation:** Structured JSON schemas for multi-lingual localization (10 languages, including bidirectional parallel English/Arabic rendering) and normalized environmental telemetry arrays.
* **Hosting & CI/CD:** Deployed via GitHub Pages and Vercel.

---

## 5. Research & Engineering Team (HexaLogic)

* **Marwa** 
* **Marwan** 
* **Rahma**
* **Mahmoud**
* **Mustafa**
* **Rasha**

---

## 6. Local Execution

```bash
git clone [https://github.com/marwa95ae/Mars_Hexalogic.git](https://github.com/marwa95ae/Mars_Hexalogic.git)
cd Mars_Hexalogic
# Serve via any static HTTP server or open index.html directly in a standards-compliant browser
