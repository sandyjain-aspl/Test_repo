# skj.com

A single-page site showing the first 10 listings on [shop.com](https://shop.com) for the search **"mens shoes"** with the **On sale** filter applied.

## What's here

- `index.html`: the whole site in one self-contained file. Product photos are embedded, so the only external requests are Google Fonts.

Each card shows the shoe photo, store, sale price, original price and percent off (when shop.com shows one), review count, and links to the listing on shop.com.

At the bottom, a **Recommendations** section shows the top 5 Amazon.com results for "shoes" with the Men filter applied, with photo, brand, price, discount, star rating, and a link to each Amazon listing.

## Data

The listings are a snapshot taken on **Oct 3, 2026**, in the order shop.com ranked them. Prices and availability change, so the page links out to each listing for current details.

The data is not pulled live: shop.com renders search results in the browser and has no public feed, so a static page cannot query it directly. Refreshing means re-running the search and updating the `ITEMS` and `IMGS` arrays in `index.html`.

Recommendations are a snapshot from **Oct 7, 2026**, kept in Amazon's order. Two of the five are the same adidas Daily 4.0 model in different colors, because Amazon listed them separately. To refresh, update the `RECS` and `REC_IMGS` arrays.

Four results (Primal Zen, Primal Zen Suede, Trail Blazer, adidas Barreda) appeared under the On sale filter but showed only one price on shop.com, so they are listed without a discount.

## Live site

Hosted on GitHub Pages from the `main` branch of this repo:

- https://sandyjain-aspl.github.io/Test_repo/skj/
- https://sandyjain-aspl.github.io/Test_repo/ redirects to the address above

Changes merged to `main` go live within a minute or two.

## Deploy to skj.com

1. The site is already hosted on GitHub Pages (see above).
2. Register skj.com with a domain registrar, if it is available.
3. In the repo's Settings > Pages, add skj.com as the custom domain, then point the domain's DNS at GitHub Pages following GitHub's custom-domain instructions.
