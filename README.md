# ✈️ Flight Calculator

A lightweight, offline-ready mobile web application (PWA) for quick aviation flight path and climb calculations.

## Features

### 1. FPA (Flight Path Angle) Solver
- **Distance input**: In **NM** (Nautical Miles). Automatically converts to feet in the background using `1 NM = 6076 ft`.
- **Height input**: In **ft**.
- **FPA input**: In **degrees (°)**.
- **Auto-generates Gradient**: Whenever FPA is calculated or solved, **Gradient (%)** is automatically computed:
  $$\text{Gradient (\%)} = \text{FPA} \times 1.75$$

**Formulas:**
- $\text{Distance (ft)} = \text{Distance (NM)} \times 6076$
- $\text{Distance (NM)} = \frac{\text{Height (ft)}}{\tan(\text{FPA}) \times 6076}$
- $\text{FPA} = \arctan\left(\frac{\text{Height (ft)}}{\text{Distance (NM)} \times 6076}\right)$
- $\text{Height (ft)} = \text{Distance (NM)} \times 6076 \times \tan(\text{FPA})$

---

### 2. Climb Gradient & Rate of Climb (ROC) Solver
Enter any **two** known values to calculate the remaining parameter:
- **Ground Speed (GS)** (`kts`)
- **Gradient** (`%`)
- **Rate of Climb (ROC)** (`FPM`)
- **Auto-generates FPA**: Whenever Gradient is calculated or solved, **FPA (°)** is automatically computed:
  $$\text{FPA} = \text{Gradient} \times 0.57$$

**Formulas:**
- $\text{ROC} = \frac{\text{GS} \times \text{Gradient} \times 101.27}{100}$
- $\text{Gradient (\%)} = \frac{\text{ROC} \times 100}{\text{GS} \times 101.27}$
- $\text{GS} = \frac{\text{ROC} \times 100}{\text{Gradient} \times 101.27}$

---

## Mobile Installation (Works 100% Offline)

This app includes a Web App Manifest (`manifest.json`) and Service Worker (`sw.js`) so it can be installed directly onto iOS and Android devices and used completely offline.

- **iOS (Safari):** Open the app URL $\rightarrow$ tap the **Share** button $\rightarrow$ **Add to Home Screen**.
- **Android (Chrome):** Open the app URL $\rightarrow$ tap the **Menu (⋮)** button $\rightarrow$ **Add to Home screen**.