# Commerce Performance Dashboard

An interactive, single-file business analytics dashboard for e-commerce/retail performance — revenue, profit, regional and channel breakdowns — built with vanilla JavaScript and Chart.js. No backend, no build step, no dependencies to install.

**[Live Demo →](https://shivangichaurasiya82-cell.github.io/commerce-performance-dashboard/)**

---

## What this is

A synthetic commerce dataset (FY2024–FY2025, 26,000+ orders) aggregated and embedded directly inside a single `.html` file, paired with an interactive filtering UI. Open the file in any browser and it just works — no server required.

## Features

- **6 live KPI cards** — Net Revenue, Gross Profit, Orders, Avg Order Value, Profit Margin, Return Rate — each with a period-over-period delta indicator
- **Multi-dimensional filters** — Region, Country (auto-narrows based on selected region), Category, Customer Segment, Sales Channel — all combinable
- **Date range slider** — scrub across Jan 2024–Dec 2025
- **6 charts** — revenue & profit trend, channel mix, region/country breakdown, category breakdown, segment mix, and a top-10 sales rep leaderboard
- Fully **offline-capable** — Chart.js is embedded inline, not loaded from a CDN
- Responsive layout — works on desktop and mobile

## Tech stack

- Vanilla HTML / CSS / JavaScript
- [Chart.js](https://www.chartjs.org/) (bundled inline)
- Data pre-aggregated with Python/pandas, embedded as JSON

## Run it locally

No installation needed. Just download `index.html` and open it in any modern browser (Chrome, Edge, Firefox, Safari).

```bash
git clone https://github.com/shivangichaurasiya82-cell/commerce-performance-dashboard.git
cd commerce-performance-dashboard
open index.html   # macOS
# or just double-click the file on Windows/Linux
```

## Deploy it live (GitHub Pages — free, no server)

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Under "Source," select your branch (usually `main`) and save
4. After a minute, your dashboard will be live at:
   `https://shivangichaurasiya82-cell.github.io/commerce-performance-dashboard/`
5. Update the "Live Demo" link at the top of this README with that URL

## Project structure

```
.
├── index.html                            # the dashboard — open this, or deploy via GitHub Pages
├── data/
│   └── business_analytics_data.xlsx      # source data behind the dashboard, formatted for easy review
├── README.md
└── LICENSE
```

## Data

The dataset is synthetic, generated to reflect realistic retail patterns: seasonality (holiday spikes, summer bump), weekend lift, and ~18% year-over-year growth. Dimensions include region, country, product category, customer segment, sales channel, sales rep, and payment method. `data/business_analytics_data.xlsx` contains the raw transaction-level records plus pre-built summary sheets (by region, category, segment, sales rep, channel). The dashboard itself uses a further-aggregated copy of this same data, embedded directly in `index.html`.

## License

MIT — see [LICENSE](LICENSE). Feel free to use, modify, and adapt this project for your own purposes.
