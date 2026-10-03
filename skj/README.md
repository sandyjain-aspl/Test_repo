# skj.com

A single-page site showing the first 10 listings on [shop.com](https://shop.com) for the search **"mens shoes"** with the **On sale** filter applied.

## What's here

- `index.html`: the whole site in one self-contained file. Product photos are embedded, so the only external requests are Google Fonts.

Each card shows the shoe photo, store, sale price, original price and percent off (when shop.com shows one), review count, and links to the listing on shop.com.

## Data

The listings are a snapshot taken on **Oct 3, 2026**, in the order shop.com ranked them. Prices and availability change, so the page links out to each listing for current details.

The data is not pulled live: shop.com renders search results in the browser and has no public feed, so a static page cannot query it directly. Refreshing means re-running the search and updating the `ITEMS` and `IMGS` arrays in `index.html`.

Four results (Primal Zen, Primal Zen Suede, Trail Blazer, adidas Barreda) appeared under the On sale filter but showed only one price on shop.com, so they are listed without a discount.

## Deploy to skj.com

1. Host the `skj/` folder on any static host (GitHub Pages, Netlify, Cloudflare Pages, Vercel).
2. Register skj.com with a domain registrar, if it is available.
3. Point the domain's DNS at the host using that host's custom-domain instructions.
