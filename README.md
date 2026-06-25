# US Job Postings — Metro & Sector (through 2023)

Two slices of Indeed Hiring Lab's **US Job Postings Tracker**, filtered to include
only observations through **December 31, 2023** (rows dated 2024-01-01 or later are
dropped).

## Files

| File | Description | Columns | Rows | Date range |
|---|---|---|---|---|
| `metro_job_postings_us.csv` | Daily Indeed Job Postings Index by US metro (CBSA) | `date, metro, cbsa_code, indeed_job_postings_index` | 847,990 | 2020-02-01 → 2023-12-31 |
| `job_postings_by_sector_US.csv` | Daily Indeed Job Postings Index by sector | `date, jobcountry, indeed_job_postings_index, variable, display_name` | 114,400 | 2020-02-01 → 2023-12-31 |

The index is set to **100 on February 1, 2020**, so values are relative to that
baseline. In the sector file, `variable` distinguishes `new postings` from
`total postings`.

## Source

Data from Indeed Hiring Lab, [`hiring-lab/job_postings_tracker`](https://github.com/hiring-lab/job_postings_tracker/tree/master/US)
(US folder), retrieved 2026-06-25. Only the date filter described above was applied;
values are otherwise unmodified. Please refer to the source repository for the full
(ongoing) series, methodology, and terms of use.
