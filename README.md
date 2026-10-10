# Market reactions to stablecoin reserve disclosures (USDT, USDC)

Replication files for *Do Reserve Disclosures Move Stablecoin Markets? Event-Study Evidence from USDT and USDC* (Ham & Chun).

| File | Contents |
|---|---|
| `stablecoin_master_v1.ipynb` | Full analysis: event list, market-model CARs, H1–H3 tests, abnormal trading volume, robustness checks, Figures 1–6 |
| `master_daily.csv` | Daily price/volume snapshot (USDT, USDC, BTC; 2020-07-01 to 2025-04-29) used for all reported results |
| `event_list_v9.csv` | 22 events dated by public release, with source URLs, quality-index coding, CARs and abnormal volumes (Table S1) |
| `manuscript_v4.docx` | Current manuscript |

Run the notebook top to bottom (Google Colab or local Python). With `USE_SNAPSHOT = True` (default) it reads `master_daily.csv` and reproduces the paper's numbers exactly; set it to `False` to re-download prices from Yahoo Finance.
