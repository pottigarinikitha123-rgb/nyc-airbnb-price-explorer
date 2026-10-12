# 🗽 NYC Airbnb Price Explorer

An interactive dashboard that answers a simple question with real data: **where in New York City can you find an affordable Airbnb, and how much more does a whole apartment cost than a room?**

**▶ Live dashboard:** https://nyc-airbnb-price-explorer-2026.higgsfield.app

## Key findings

At the default $1,000 nightly price cap, using median advertised prices:

- **Manhattan is the most expensive borough at about $244 a night**, more than double Staten Island (about $105) and the Bronx (about $107). Brooklyn (about $154) and Queens (about $124) sit in between.
- **An entire home or apartment costs about $211 a night**, nearly double a private room (about $112). Shared rooms are the cheapest option at about $89.
- Hotel rooms listed on Airbnb are the priciest room type, at a median of about $525.

Use the filters to dig deeper, for example to find the cheapest neighborhoods for a private room in Brooklyn.

## Features

- Median nightly price by borough
- Median nightly price by room type
- The most affordable neighborhoods, counting only neighborhoods with enough listings to be reliable
- Distribution of nightly prices
- Filters for borough, room type, maximum price, and minimum listings per neighborhood
- Interactive SVG charts with hover tooltips
- Works offline: the cleaned data is built into the page, so no server or upload is needed

## Data and methodology

**Source:** [Inside Airbnb](https://insideairbnb.com/get-the-data/), New York City listings snapshot dated September 14, 2026. The raw dataset is included as `data/listings.csv.gz` so the analysis can be reproduced.

- The raw file has **29,918 listings and 90 columns**.
- **10,512 listings have no price** and are excluded, leaving **19,406 priced listings**.
- The dashboard uses **medians** rather than averages, because a small number of very expensive listings would distort an average.
- A default **$1,000 nightly price cap** removes extreme outliers. Visitors can change it.
- Neighborhood rankings only include neighborhoods with at least 20 listings by default, so one or two cheap listings can't put a neighborhood at the top.

These are advertised nightly prices, not confirmed booking totals, so taxes and fees may not be included.

## Run locally

Download `index.html` and open it in any modern browser. No installation or server needed.

## Tech stack

HTML, CSS, and vanilla JavaScript, with hand-built SVG charts and no libraries or build step.

## Project structure

```
├── index.html             # The full dashboard, with cleaned data built in
├── data/
│   └── listings.csv.gz    # Raw Inside Airbnb NYC snapshot (compressed)
└── README.md
```

## About

Built by **Nikhitha Pottigari** · [LinkedIn](https://www.linkedin.com/in/nikhitha-p-abb311256) · [GitHub](https://github.com/pottigarinikitha123-rgb)

## Data license

Inside Airbnb data is shared under [Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/). Attribution: Inside Airbnb, https://insideairbnb.com/.
