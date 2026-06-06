# SGCarPricing

A Singapore car fair price calculator — hosted at [zeinliu.github.io/SGCarPricing](https://zeinliu.github.io/SGCarPricing).

## What it does

Calculates the true cost of buying a car in Singapore by breaking down all LTA-mandated fees and taxes. Supports both new cars and used/resale cars.

## Pricing logic (LTA 2026)

| Component | Rule |
|---|---|
| **ARF** | Tiered: 100% / 140% / 190% / 250% / 320% of OMV by bracket |
| **Excise Duty** | 20% of OMV |
| **GST** | 9% on (OMV + Excise Duty) |
| **VES 2026** | Band A: −$22,500 (EV only) · B: $0 · C1: +$7,500 · C2: +$17,500 · C3: +$35,000 |
| **EEAI** | 45% of ARF, capped at $7,500 (EVs only, 2026) |
| **Min ARF** | $0 for EVs · $5,000 for all others |
| **PARF rebate** | 50–75% of net ARF, capped at $60,000 (Feb 2023+ cars) |
| **COE rebate** | Proportional to months remaining out of 120 |

## Tech

- Single `index.html` file — no frameworks, no dependencies
- Pure HTML / CSS / JS
- Mobile-first, works on phone browsers
- Deployed via GitHub Pages (no build step)

## Features

- **New Car tab** — full price breakdown including ARF, VES, EEAI, GST, and COE
- **Used/Resale tab** — calculates remaining PARF and COE rebate value
- Sliders and dropdowns for quick input
- Warnings shown when surcharges are high
