# Market Recovery Screen — Time Back to Even

Revised version of the Q2 2026 PF Market Return Analysis, refocused per CB's 8/17 spec on three variables: **embedded rent-roll mark-to-market**, **construction starts**, and **time back to even** using RealPage's actual multi-year forecast instead of 10-year historical average growth.

## Files

- `Q2_2026_PF_Market_Return_Analysis_v2.xlsx` — the revised workbook (65-market screen: original 50 + 15 expansion markets added 8/17 — Milwaukee, Madison, Sioux Falls, Chattanooga, Asheville, Fayetteville-Rogers AR, Baton Rouge, Port St. Lucie, Lakeland-Winter Haven, Myrtle Beach, Naples, Tallahassee, New Orleans, Fort Collins, Spokane. Lake Charles, LA is not in the RealPage DataDirect market set. TTM unit starts blank for the added markets pending the next DataDirect pull)
- `data/datadirect_72.xlsx` — RealPage DataDirect export (Aug 2026 pull): 150 markets, actuals through 2026Q2, same-store YOY effective rent forecast + Existing Units forecast through 2029Q4
- `data/Q2_2026_PF_Market_Return_Analysis_v1.xlsx` — prior version (source of the TTM unit starts and 10-yr historical rent change tabs, and the PF LIRR engine that was dropped from v2)

## Methodology (v2)

- **Mark-to-market:** Asking (gross) and Effective RPSF vs. Rent Roll (Rev/OSF), Q2 2026 actuals.
- **Time back to even:** Effective RPSF is walked forward quarterly, `Path(t) = Path(t-4) × (1 + forecast YOY(t))`, against a *flat* current rent roll PSF (conservative by design). Reported figure = time until the path recovers to the rent roll level and stays above it through the 3.5-yr horizon, interpolated within the crossing quarter. `†` = still underwater at 2029Q4; extended at the terminal forecast growth rate. Engine on the `Fcst Walk` tab.
- **Supply:** TTM unit starts as % of inventory (2025Q3–2026Q2) plus forward 12-month inventory growth from RealPage's Existing Units forecast.
- The old historical-average method is retained in the right-hand columns for comparison. Note: the v1 workbook's RealPage 10-yr averages were mis-ranged (`AVERAGEIF` off-range bug — e.g. Charlotte showed −0.2% vs. an actual 5.3%); corrected in v2.

## Known simplifications

Directional tool by design: ignores renewal vs. new-lease mix, retention, and rent-roll drift as leases turn. Q2 2026 levels reflect RealPage restatements and differ modestly from the v1 pull.
