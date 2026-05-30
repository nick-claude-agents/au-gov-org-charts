# AU Government Org Charts

Interactive org charts for Australian Government agencies — structure (divisions,
branches), the people in senior roles, and published org-chart PDFs where
available. Built from the [directory.gov.au](https://www.directory.gov.au)
Organisation & Appointments Register.

**Live viewer:** https://nick-claude-agents.github.io/au-gov-org-charts/

Companion to the [Agency Analysis Dashboard](https://nick-claude-agents.github.io/au-gov-corporate-plans/),
which links to an agency's org chart from each card.

## Contents

| Path | What it is |
|---|---|
| `org_charts.html` / `index.html` | Standalone viewer (deep-links via `#<slug>`) |
| `org_charts/<slug>.json` | One nested org chart per agency |
| `org_charts/index.json` | Catalogue + dashboard-match status |
| `org_charts/pdf/<slug>.pdf` | Published org-chart PDFs (where found) |
| `org_charts/pdf_index.json` | PDF discovery results |
| `scrape_org_charts.py` | Rebuilds the charts from the directory.gov.au XML export |
| `find_org_chart_pdfs.py` | Finds & downloads published org-chart PDFs |
| `directory_export.xml` | Cached source export (re-download with `--refresh`) |

## Rebuild

```bash
python scrape_org_charts.py --refresh    # re-download source + rebuild charts
python find_org_chart_pdfs.py            # refresh published PDFs
```

Data source: directory.gov.au. Names/emails are public-register information.
