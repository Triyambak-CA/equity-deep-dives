# equity-deep-dives

Published fundamental research on Indian listed companies, served as a static
site by GitHub Pages.

This repo holds **finished reports only**. The research itself, the working
notes and roughly 931 MB of source filings live in a separate private repo and
never appear here.

## Publishing a report

From the private research repo:

```sh
./publish-report.sh <path-to-report.html> "<Company Name>" <YYYY-MM-DD> "<one-line note>"
```

That copies the report in under a URL-safe name, adds a row to `reports.json`
and regenerates `index.html`. Then commit and push here.

Other modes:

```sh
./publish-report.sh --list            # what is currently published
./publish-report.sh --rebuild-index   # regenerate index.html from reports.json
```

The script refuses to copy any file containing an `update_key`, an ht-ml.app URL
or a local machine path.

## Files

| File | What it is |
|---|---|
| `index.html` | Generated landing page. Do not edit by hand, it is overwritten. |
| `reports.json` | The manifest. One row per report; the index is built from it. |
| `<company>-<date>.html` | A self-contained report. No external assets. |

## Not investment advice

Personal research notes published for the record. No ratings, no price targets.
The author is not a SEBI-registered research analyst or investment adviser.
