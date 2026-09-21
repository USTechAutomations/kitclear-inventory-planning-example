# KitClear inventory planning example

A free, static worked example for KitClear Offline. It shows how one fixed, synthetic set of stock and orders is split across competing jobs — first allowing partial fulfillment, then requiring whole orders — so you can see exactly what the tool produces before deciding whether to buy it.

This repository is a sample only. It is **not** the paid tool: it cannot read your files, the downloaded sample has no input-upload feature. Every number here comes from one frozen synthetic input and never changes.

## Download

**[Download the sample — `example.zip`](https://raw.githubusercontent.com/USTechAutomations/kitclear-inventory-planning-example/main/example.zip)**

## What's inside

- `inputs/example.json` — the synthetic scenario: stock, reserved units, bills of materials, and three orders (`ORDER-A`, `ORDER-B`, `ORDER-C`).
- `outputs/partial/` and `outputs/whole/` — results for each policy, each as `allocation.json`, `orders.csv`, `materials.csv`, a `README.txt`, and a viewable `rendered.html`.
- `MANIFEST.sha256` — checksums for the sample files, so you can confirm nothing was altered.

## What the results show

Open the two `orders.csv` files side by side. Allowing partial fulfillment fills 6, 2, and 0 units for the three orders; requiring whole orders fills 6, 0, and 0. The two reserved `board` units are held back and never assigned. `materials.csv` lists what was picked, what stays reserved, and the extra components a full fill would need.

## How allocation works, and its limits

Orders are filled in descending priority, with ties broken by input order — a clear rule, not a global optimum. Bills of materials are single-level integers, with one stock location. Listed shortages are review information, not purchase orders. There are no forecasts, dates, substitutions, purchasing, or assembly steps.

The paid product runs the same engine on your own inventory and orders. For current pricing and a step-by-step walkthrough of this scenario, use the links below.

- Walkthrough of this example: https://ustechautomations.com/feeds/kitclear/inventory-planning-example/
- Paid product, KitClear Offline: https://ustechautomations.gumroad.com/l/kitclear-offline?utm_source=github&utm_medium=example&utm_campaign=non_ecommerce_20260921
