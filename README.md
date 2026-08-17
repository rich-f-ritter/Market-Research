# Market Research

Repository for multifamily market and submarket research.

## Purpose

This repo houses research artifacts for multifamily markets and submarkets: market overviews, submarket deep-dives, supply pipeline analyses, rent and occupancy trends, demographic and employment drivers, and supporting data exports.

## Structure

```
markets/          One folder per metro market (e.g. markets/dallas-fort-worth/)
  <market>/
    submarkets/   Submarket-level research within that market
    data/         Raw exports for that market (CoStar, RealPage, HelloData, Census, etc.)
    reports/      Finished deliverables (workbooks, memos, maps)
notes/            Cross-market notes, methodology, and scratch research
```

## Conventions

- Name market folders in kebab-case by metro (e.g. `phoenix`, `dallas-fort-worth`, `tampa`).
- Keep raw data exports separate from finished deliverables so analyses are reproducible.
- Date-stamp data exports and reports (e.g. `costar-supply-2026-08-17.xlsx`) since market data goes stale quickly.
