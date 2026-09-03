# Orozco House — Golden Hill, San Diego

Marketing site for **Private 2BR Downtown House + Parking**, a two-bedroom Victorian cottage in
Golden Hill, San Diego.

Listing: https://www.airbnb.com/rooms/696503088612245611

## Pages

| File | Purpose |
|---|---|
| `index.html` | Home |
| `shop.html` | "Shop the house" — Amazon affiliate page |
| `404.html` | Not found |

Static HTML. No build step, no dependencies — publish the folder as-is.

## Before this goes live

The site currently ships with **visible placeholders**. They are deliberate, not oversights.

- `[MIN]` — walk times to the Gaslamp Quarter, Balboa Park and the Convention Center
- `[HRB NO.]` / `[YEAR]` — the historic-register designation
- `[HOST NAME]` — the name on the Amazon Associates account
- `YOUR-ASSOCIATES-TAG` — the Amazon Associates tracking ID, in `shop.html`
- `[YOUR-DOMAIN]` — in `robots.txt` and `sitemap.xml`

Set `og:image` in `index.html` to an absolute URL once a domain exists.

## The shop page

Affiliate links are **temporary**: they point at Amazon *searches* for the type of item, not at
specific products, because the exact brand and model cannot be verified from a photograph. Replace
each `href` with the real product URL as they are confirmed, keeping `?tag=` and
`rel="nofollow sponsored"`.

Swap the tag in one pass:

```bash
sed -i '' 's/YOUR-ASSOCIATES-TAG/your-real-tag-20/g' shop.html
```

Product photography on that page is our own — Amazon's Operating Agreement does not permit using
their product images outside the Product Advertising API or their own widgets.

## Image credits

Property photography is from the listing. Area photography is Creative Commons and **the credits
must stay on the page**. See `IMAGE-CREDITS.md`.
