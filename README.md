# SSF Steady-State Removal Model Explorer

**Interactive web tool** to explore the *steady-state* concentration profile and log-removal in **slow sand filtration (SSF)** using a **two-site kinetic attachment–detachment model** (Schijven et al., 2013).

👉 **Live demo:** **[LIVE_URL_HERE](https://porouslab.github.io/ssf-model-explorer/)**

---

## What this tool does

This app lets you vary hydraulic and kinetic parameters (sliders + presets) and instantly see:

- **C(x)/C₀ (%)** vs depth  
- **log₁₀ removal** vs depth  
- **effective removal coefficient λ** and its breakdown (Site 1, Site 2, liquid inactivation)  
- depths corresponding to **2-log** and **4-log** removal (when within range)

---

## Model (steady state)

The tool implements the analytical steady-state solution:

**Effective removal coefficient**
\[
\lambda = \mu_l + \frac{k_{att,1}}{1 + k_{det,1}/\mu_{s,1}} + \frac{k_{att,2}}{1 + k_{det,2}/\mu_{s,2}}
\]

**Steady-state concentration profile**
\[
\ln \left(\frac{C}{C_0}\right) =
\left[\frac{1-\sqrt{1+\frac{4\alpha_L\lambda}{v}}}{2\alpha_L}\right]x
\]

**Where**
- \( v \) = pore velocity (m/d)  
- \( \alpha_L \) = dispersivity (m)  
- \( x \) = depth (m)  
- \( k_{att,i}, k_{det,i} \) = attachment/detachment rates (d⁻¹)  
- \( \mu_{s,i}, \mu_l \) = inactivation rates in solid/liquid phase (d⁻¹)

> Note: this is a **steady-state depth profile** (not a time-dependent breakthrough curve).

---

## How to use (quick guide)

1. Pick a **preset** (e.g., “Clean Bed”, “Mature Filter”) or move sliders manually  
2. Watch how **C/C₀** and **log removal** change with:
   - increasing **v** (typically reduces removal per depth)
   - increasing **λ** (increases removal)
   - increasing **αL** (changes curvature / profile shape)
3. Use the “Contribution to λ” panel to see which site dominates.

---

## How to cite

If you use this tool in teaching or a report, cite:

- Schijven et al. (2013), *Removal of microorganisms by slow sand filtration* (two-site kinetic model)
- This repository and the live URL (add DOI if you later archive via Zenodo)

---

## Local development

Requirements: **Node.js** (LTS recommended)

```bash
npm install
npm run dev
