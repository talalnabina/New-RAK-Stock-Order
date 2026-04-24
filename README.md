# New RAK Stock Order

Static ecommerce storefront + printable catalog for RAK Ceramics discounted tile stock.

## Live site

Once GitHub Pages is enabled, the live store is served from:

```
https://<your-github-username>.github.io/New-RAK-Stock-Order/
```

## What's in this repo

| File | Description |
|---|---|
| `index.html` | Self-contained storefront (77 products, embedded photos, cart + checkout workflow). Runs entirely in the browser — no server. |
| `catalog.pdf` | Printable A4 catalog (11 pages, 3×3 grid). |
| `catalog.docx` | Editable Word catalog (5-column table with embedded photos). |

## Pricing

All prices are in **QAR (Qatari Riyal)**, computed from the source Excel's discounted unit price:

```
selling_price  =  discounted_unit  ×  1.20  (20% shipment)  ×  1.40  (40% margin)
              =  discounted_unit  ×  1.68
```

## Stock snapshot

- **77 products** across 34 RAK series
- **147,305.55 m²** total quantity
- **QAR 7,243,811** total stock value (at selling price)
- **65 products** have embedded product photos; the remaining 12 fall back to a color swatch

## Source data

Built from two RAK Ceramics stock sheets:
- `DISCOUNTED STOCK 22.xlsx` (Q16885 — "After 30% Discount Unit Price")
- `Q-16870 (1).xlsx` (Q-16870 — "UOM Price – Price Difference")

## Storefront features

- Search by SKU / name / color / series
- Filter by series, size, finish, color
- Product detail modal with large photo and **prominent availability banner** (in-stock / low-stock / out-of-stock)
- Cart with quantity adjustment (respects available stock)
- Checkout form → generates order summary that can be copied / printed / emailed

## Enabling the live site

After pushing this repo to GitHub:

1. Go to **Settings → Pages**
2. Under **Source**, select **Deploy from a branch**
3. Branch: `main`, Folder: `/ (root)`
4. Save. GitHub builds the site within a minute.
