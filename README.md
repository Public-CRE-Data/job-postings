# US Job Postings — Metro & Sector (through 2023)

Indeed Hiring Lab's **US Job Postings Tracker**, filtered to observations through
**December 31, 2023** and split into small, spreadsheet-friendly files — one per
sector and one per major metro. The index is set to **100 on February 1, 2020**, so
each value is relative to that baseline.

## Structure

```
by_sector/   40 files, one per sector  + _index.csv
by_metro/    30 files, one per top-30 US metro (by population) + _index.csv
```

### `by_sector/` — daily index by sector
Columns: `date, jobcountry, indeed_job_postings_index, variable, display_name`
(`variable` = `new postings` vs `total postings`; `jobcountry` = US). One file per
sector, named by a slug of the sector (e.g. `software_development.csv`,
`banking_and_finance.csv`). Full file↔sector map in [`by_sector/_index.csv`](by_sector/_index.csv).

Sectors (40): Accounting · Administrative Assistance · Architecture · Arts & Entertainment ·
Banking & Finance · Childcare · Civil Engineering · Cleaning & Sanitation ·
Community & Social Service · Customer Service · Data & Analytics · Education & Instruction ·
Electrical Engineering · Food Preparation & Service · Hospitality & Tourism · Human Resources ·
IT Infrastructure, Operations & Support · IT Systems & Solutions · Industrial Engineering ·
Installation & Maintenance · Legal · Loading & Stocking · Logistic Support · Management ·
Marketing · Mechanical Engineering · Media & Communications · Medical Information ·
Medical Technician · Nursing · Pharmacy · Physicians & Surgeons · Production & Manufacturing ·
Project Management · Retail · Sales · Scientific Research & Development · Security & Public Safety ·
Social Science · Software Development.

### `by_metro/` — daily index by metro
Columns: `date, metro, cbsa_code, indeed_job_postings_index`. One file per metro, named
by a city slug (e.g. `new_york_ny.csv`). Rank + CBSA map in [`by_metro/_index.csv`](by_metro/_index.csv).

Top-30 US metros (by population, matched on CBSA code):

| # | Metro | File | # | Metro | File |
|---|---|---|---|---|---|
| 1 | New York, NY | `new_york_ny.csv` | 16 | Minneapolis, MN | `minneapolis_mn.csv` |
| 2 | Los Angeles, CA | `los_angeles_ca.csv` | 17 | Tampa, FL | `tampa_fl.csv` |
| 3 | Chicago, IL | `chicago_il.csv` | 18 | San Diego, CA | `san_diego_ca.csv` |
| 4 | Dallas–Fort Worth, TX | `dallas_fort_worth_tx.csv` | 19 | Denver, CO | `denver_co.csv` |
| 5 | Houston, TX | `houston_tx.csv` | 20 | Baltimore, MD | `baltimore_md.csv` |
| 6 | Atlanta, GA | `atlanta_ga.csv` | 21 | St. Louis, MO | `st_louis_mo.csv` |
| 7 | Washington, DC | `washington_dc.csv` | 22 | Orlando, FL | `orlando_fl.csv` |
| 8 | Philadelphia, PA | `philadelphia_pa.csv` | 23 | Charlotte, NC | `charlotte_nc.csv` |
| 9 | Miami, FL | `miami_fl.csv` | 24 | San Antonio, TX | `san_antonio_tx.csv` |
| 10 | Phoenix, AZ | `phoenix_az.csv` | 25 | Portland, OR | `portland_or.csv` |
| 11 | Boston, MA | `boston_ma.csv` | 26 | Sacramento, CA | `sacramento_ca.csv` |
| 12 | Riverside, CA | `riverside_ca.csv` | 27 | Pittsburgh, PA | `pittsburgh_pa.csv` |
| 13 | San Francisco, CA | `san_francisco_ca.csv` | 28 | Austin, TX | `austin_tx.csv` |
| 14 | Detroit, MI | `detroit_mi.csv` | 29 | Las Vegas, NV | `las_vegas_nv.csv` |
| 15 | Seattle, WA | `seattle_wa.csv` | 30 | Cincinnati, OH | `cincinnati_oh.csv` |

Each metro file covers 2020-02-01 → 2023-12-31 (1,430 daily rows); each sector file
2,860 rows (both `new` and `total` postings).

## Source

Data from Indeed Hiring Lab, [`hiring-lab/job_postings_tracker`](https://github.com/hiring-lab/job_postings_tracker/tree/master/US)
(US folder), retrieved 2026-06-25. Only the date filter (≤ 2023-12-31) and the
per-series split were applied; index values are otherwise unmodified. See the source
repository for the full ongoing series, methodology, and terms of use.
