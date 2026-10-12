# ✈️ Flight Calculator

A lightweight, offline-ready mobile web application (PWA) for quick aviation flight path and climb calculations.

## Features

### 1. FPA (Flight Path Angle) Solver
Enter any **two** known values to calculate the remaining parameter:
- **Distance** (`NM` / `ft`)
- **Height** (`ft`)
- **FPA** (`°`)

**Formulas:**
- $\text{Distance} = \frac{\text{Height}}{\tan(\text{FPA})}$
- $\text{FPA} = \arctan\left(\frac{\text{Height}}{\text{Distance}}\right)$
- $\text{Height} = \text{Distance} \times \tan(\text{FPA})$

---

### 2. Climb Gradient & Rate of Climb (ROC) Solver
Enter any **two** known values to calculate the remaining parameter:
- **Ground Speed (GS)** (`kts`)
- **Gradient** (`%`)
- **Rate of Climb (ROC)** (`FPM`)

**Formulas:**
- $\text{ROC} = \frac{\text{GS} \times \text{Gradient} \times 101.27}{100}$
- $\text{Gradient (\%)} = \frac{\text{ROC} \times 100}{\text{GS} \times 101.27}$
- $\text{GS} = \frac{\text{ROC} \times 100}{\text{Gradient} \times 101.27}$

---

## Mobile Installation (Works 100% Offline)

This app includes a Web App Manifest (`manifest.json`) and Service Worker (`sw.js`) so it can be installed directly onto iOS and Android devices and used completely offline.

- **iOS (Safari):** Open the app URL $\rightarrow$ tap the **Share** button $\rightarrow$ **Add to Home Screen**.
- **Android (Chrome):** Open the app URL $\rightarrow$ tap the **Menu (⋮)** button $\rightarrow$ **Add to Home screen**.
