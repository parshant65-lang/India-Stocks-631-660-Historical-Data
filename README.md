# India-Stocks-631-660-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 631 to 660)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-631-660-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (631 to 660)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 631 | `ANTGRAPHIC` | Antarctica Limited | `ANTGRAPHIC.NS` |
| 632 | `ANUHPHR` | Anuh Pharma Limited | `ANUHPHR.NS` |
| 633 | `ANUP` | The Anup Engineering Limited | `ANUP.NS` |
| 634 | `AONESTEELS` | A-One Steels India Limited | `AONESTEELS.NS` |
| 635 | `APCL` | Anjani Portland Cement Limited | `APCL.NS` |
| 636 | `APCOTEXIND` | Apcotex Industries Limited | `APCOTEXIND.NS` |
| 637 | `APEX` | Apex Frozen Foods Limited | `APEX.NS` |
| 638 | `APLLTD` | Alembic Pharmaceuticals Limited | `APLLTD.NS` |
| 639 | `APOLLO` | Apollo Micro Systems Limited | `APOLLO.NS` |
| 640 | `APOLLOPIPE` | Apollo Pipes Limited | `APOLLOPIPE.NS` |
| 641 | `APOLSINHOT` | Apollo Sindoori Hotels Limited | `APOLSINHOT.NS` |
| 642 | `APOORVA` | Apoorva Leasing Finance and Investment Company Limited | `APOORVA.NS` |
| 643 | `APTECHT` | Aptech Limited | `APTECHT.NS` |
| 644 | `AQYLON` | Aqylon Nexus Limited | `AQYLON.NS` |
| 645 | `ARCHIDPLY` | Archidply Industries Limited | `ARCHIDPLY.NS` |
| 646 | `ARCHIES` | Archies Limited | `ARCHIES.NS` |
| 647 | `ARCIL` | Asset Reconstruction Company (India) Limited | `ARCIL.NS` |
| 648 | `ARCL` | ARCL Organics Limited | `ARCL.NS` |
| 649 | `ARDEE` | Ardee Industries Limited | `ARDEE.NS` |
| 650 | `ARENTERP` | Rajdarshan Industries Limited | `ARENTERP.NS` |
| 651 | `ARFIN` | Arfin India Limited | `ARFIN.NS` |
| 652 | `ARIES` | Aries Agro Limited | `ARIES.NS` |
| 653 | `ARIHANT` | Arihant Foundations & Housing Limited | `ARIHANT.NS` |
| 654 | `ARIHANTCAP` | Arihant Capital Markets Limited | `ARIHANTCAP.NS` |
| 655 | `ARIHANTSUP` | Arihant Superstructures Limited | `ARIHANTSUP.NS` |
| 656 | `ARIS` | Arisinfra Solutions Limited | `ARIS.NS` |
| 657 | `ARKADE` | Arkade Developers Limited | `ARKADE.NS` |
| 658 | `ARMANFIN` | Arman Financial Services Limited | `ARMANFIN.NS` |
| 659 | `ARMEE` | ArMee Infotech Limited | `ARMEE.NS` |
| 660 | `AROGRANITE` | Aro Granite Industries Limited | `AROGRANITE.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream ANTGRAPHIC 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-631-660-Historical-Data/main/ANTGRAPHIC/1m/2026/10/ANTGRAPHIC_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
