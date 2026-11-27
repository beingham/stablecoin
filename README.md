# Market reactions to stablecoin reserve disclosures (USDT, USDC)

Replication files for *Do Reserve Disclosures Move Stablecoin Markets? Event-Study Evidence from USDT and USDC* (Ham & Chun), FinTech manuscript fintech-4675558.

## Round 2 revision (manuscript v11)

| File | Contents |
|---|---|
| `stablecoin_master_v3.ipynb` | Full analysis. All earlier steps are retained; **STEP V11 reproduces every number in the v11 manuscript** (Tables 4–10, Figures 1–3) and cell V11e the hourly SVB figures (Section 4.5, Figure 4c). |
| `events_v11_base.csv` | Event sample of v11: 54 routine disclosures (USDT 15, USDC 39) and 7 stress observations, with the recoded quality index, the date type of every event, and a flag for proxy-dated Circle attestations |
| `circle_attestation_dates_v11.csv` | Circle monthly attestations: reporting date, date printed in the report, PDF creation date, date used, dating method, first Internet Archive capture, and source URL |
| `Supplementary_Tables_S1_S2_v11.xlsx` | Table S1 (included events with date sources and event-level results; excluded candidates; market-news calendar; stress events with standardized CARs; dating-sensitivity, multiple-testing, and calendar-matched results) and Table S2 (source-level quality coding with the basis for each code) |
| `usdc_usd_hourly_bitstamp_svb.csv` | Hourly USDC/USD prices on Bitstamp, 10–12 March 2023 (UTC), from Bitstamp's public API |

Run `stablecoin_master_v3.ipynb` top to bottom with all CSV files in the same folder. Results were checked with Python 3.13 outside Colab.

## Round 1 revision (manuscript v10)

| File | Contents |
|---|---|
| `stablecoin_master_v2.ipynb` | Full analysis. Steps 1–11 reproduce the submitted version; STEP R contains the analyses requested by the reviewers; **STEP V10 reproduces every number in the revised manuscript** (Tables 4–9, Figure 2). Saved with outputs. |
| `events_v10_base.csv` | Rule-based event sample of the revised manuscript: 51 routine disclosures (USDT 15, USDC 36) and 7 stress observations from four episodes |
| `event_candidates_v10.csv` | Candidate events with sources, importance ranking, and the scenario used for alternative samples |
| `circle_attestation_dates_v10.csv` | Circle monthly attestations: reporting date, signature date in the text, PDF creation date, dating method, and source URL |
| `Supplementary_Tables_S1_S2_v10.xlsx` | Table S1 (included events with sources and event-level results; excluded candidates with reasons; market-news calendar; standardized CARs of stress events) and Table S2 (quality-index coding by criterion) |
| `supply_daily.csv` | Daily circulating supply of USDT and USDC (DefiLlama) |
| `btc_volume_daily.csv` | Daily Bitcoin price and volume (Yahoo Finance), used for market-adjusted abnormal volume |
| `master_daily.csv` | Daily price/volume snapshot (USDT, USDC, BTC; 2020-07-01 to 2025-04-29) used for all reported results |

## Submitted version (retained)

| File | Contents |
|---|---|
| `stablecoin_master_v1.ipynb` | Analysis of the submitted manuscript (22 events) |
| `event_list_v9.csv` | 22 events of the submitted manuscript with sources and event-level results |


## How to run

Run `stablecoin_master_v2.ipynb` top to bottom in Google Colab or local Python, with the CSV files in the same folder. With `USE_SNAPSHOT = True` (default) the notebook reads `master_daily.csv` and reproduces the reported numbers exactly. In Colab, cell R00 can also download optional files (hourly USDC/USDT prices for the SVB weekend, daily high/low prices); these are used only in supplementary checks.

Software used for the reported results: Python 3.13, NumPy 2.5, pandas 3.0, SciPy 1.18, statsmodels 0.15, Matplotlib 3.11.
