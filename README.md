# Nordic Ratio

A small finance/accounting web app that shows how **accrual accounting** changes the picture of a company's finances compared to a pure cash view — built as a personal CV project while studying HA Almen (BSc in International Business) at Copenhagen Business School.

**Live demo:** _add your Vercel URL here once deployed_

## What it does

Nordic Ratio is a single-page tool built around a fictional company, Nordic Craft ApS, that lets you explore several core finance/accounting concepts hands-on:

- **Accrual vs. cash basis** — see the same transactions produce a different month-by-month income statement depending on accounting method, with a plain-language explanation of why they differ
- **Budget vs. actual** — variance tracking against a monthly budget
- **Cash flow forecast** — a forward-looking cash position projection
- **Financing scenarios** — loan vs. equity comparisons, with a correct amortization schedule (interest and principal repayment both reflected in the cash flow)
- **Invoices (accounts receivable)** — semi-automatic invoice-to-payment matching against bank transactions, with a Matched / Partial / Open / Overdue status model and an aging breakdown (1–30 / 31–60 / 61+ days), modeled on how tools like e-conomic, Xero and Billy handle bank reconciliation and AR aging
- **CSV/Excel import** — upload your own transactions or invoices as `.csv` or `.xlsx`, with a parser tolerant of Danish export quirks (semicolon delimiters, BOM markers, Danish column headers and number formats)

All figures are shown in DKK, and the sample dataset ("Nordic Craft ApS") is entirely fictional.

## Tech

Deliberately simple: a single self-contained `index.html` file — HTML, CSS and vanilla JavaScript, no build step, no framework, no backend. Excel parsing uses the [SheetJS](https://sheetjs.com/) library loaded from a CDN; everything else is hand-written.

## Running it locally

No installation needed — just open `index.html` in a browser, or serve the folder with any static file server, e.g.:

```bash
python3 -m http.server
```

## Background

Built iteratively with [Claude](https://claude.ai) as a coding assistant, as a self-directed project to apply and demonstrate concepts from my accounting and finance coursework (bookkeeping/accrual accounting, budgeting, cash flow management, and basic corporate financing theory) in something concrete and interactive.

## License

MIT — see [LICENSE](LICENSE).
