# Arrowstack-Project-1
A Sales Performance project analysis of a Company's Sales using Analytic tools like Excel for data cleaning, SQl for analysis and Power BI for visualization

## Overview

This project analyzes order-level sales data to answer three questions:

1. How concentrated is revenue among top customers, and what's the churn risk?
2. Which regions and product categories are profitable, and which are losing money?
3. How much profit is discounting costing the business, and where should the line be drawn?

## Baseline KPIs

| Metric | Value |
|---|---|
| Total Revenue | $2.297M |
| Net Profit | $286.4K |
| Overall Profit Margin | 12.47% |
| Customers | 2,449 |
| Orders | 9,994 |
| Orders per Customer | ~4.08 |
| Average Basket Size | 3.79 units/order |
| Average Order Value (AOV) | $229.86 |
| Conversion Rate | 10.00% |

## Key Findings

### Customer Value Concentration

The top 20% of customers generate **56.77%** of total revenue — meaningful concentration, but short of a strict 80/20 Pareto split. The remaining 80% of customers still produce over 43% of sales, so the business isn't overexposed to churn from any single account.

- **Tier 1 (top 20%):** High-touch retention — dedicated support, early inventory access, volume discounts.
- **Tier 2 (20–50%):** Cross-sell and basket expansion; shifting 5% of these customers into Tier 1 would meaningfully lift revenue.
- **Long tail (bottom 50%):** Automated marketing and self-serve funnels to protect margin without overspending on account management.

### Regional Performance

| Region | Sales | Profit | Margin |
|---|---|---|---|
| West | $725.5K | $108.4K | **14.94%** (highest) |
| East | $678.8K | — | 13.48% |
| South | $391.7K | — | 11.93% |
| Central | $501K | $39.7K | **7.92%** (lowest) |

- **West** leads on both volume and profitability — the benchmark region for expansion.
- **Central** generates more revenue than South but the lowest absolute profit and a margin well under the 12.47% corporate baseline — a discounting and cost problem, not a demand problem (see [Discount Impact](#discount-impact)).
- **East** is a stable second performer on both revenue and margin.
- **South** has the smallest footprint but a healthy margin, meaning it can absorb more volume without hurting overall performance.

### Category Performance

**Loss leaders:**
- Tables (**−8.56%**) and Bookcases (**−3.02%**) — negative margin.
- Chairs (8.10%) — well under the 12.47% baseline.
- Supplies (**−2.55%**) — a net loss despite other stationery being highly profitable.
- Machines (1.79%) — razor-thin, likely high supplier cost or steep price cuts.

**Cash cows:**
- Labels (44.42%), Paper (43.39%), Envelopes (42.27%) — 40%+ margin office consumables.
- Copiers (37.20%), Accessories (25.05%) — high margin *and* high ticket value.

**Recommendations:**
- Cap discounts on Tables and Bookcases, or pass bulk shipping costs to the customer.
- Bundle high-margin consumables (Paper, Accessories) with low-margin hardware (Machines, Phones).
- Check whether Central's weak margin is driven by outsized Tables/Bookcases volume.

### Discount Impact

| Discount Bracket | Profit | Margin |
|---|---|---|
| 0% | $321.0K | **29.51%** |
| 1–20% | $100.8K | 11.91% |
| 21–50% | **−$58.8K** | −19.70% |
| >50% | **−$76.6K** | −119.20% (856 orders, $64.2K in sales) |

Margin collapses the moment discounts cross 20%. Combined, discounts above 20% cost the business **$135,376.05** in losses. Capping all discounts at 20% would have raised total profit from $286.4K to an estimated **$421.7K** (margin: 12.47% → ~18.36%).

**Central region is the primary offender:**
- Binders discounted 50.93% on average → −$1,043.64 net loss.
- Appliances discounted 44.88% → −$2,638.62 loss (−11.19% margin).
- Furnishings discounted 40.39% → −$3,906.22 loss (−25.61% margin).
- At *controlled* discount levels, Central performs normally (e.g., Paper at 12.90% discount still nets 39.86% margin) — this is a discounting-policy problem, not a cost-structure problem.

**Tables is a cross-regional problem**, and the fix already exists in the data: West held Tables discounts at exactly 20.00% and turned a profit (+$1,482.61), while East (37.38% avg. discount), South (22.25%), and Central (26.25%) all lost money on the same category.

**Machines** loses money in three of four regions (South, Central, West); only East, with the lowest average discount (28.38%) and highest volume ($66.1K), is profitable.

## Executive Recommendations

1. **Enforce a 20% promotional discount ceiling** — any exception requires regional/executive sign-off.
2. **Eliminate clearance discounts above 50%** — even for dead inventory; bundle slow movers with high-margin items instead.
3. **Freeze Central region discounting** on Binders, Appliances, and Furnishings — recovers an estimated $7,588.
4. **Standardize Tables discounting to the West's 20% policy nationwide** — recovers an estimated $19,000+.
5. **Renegotiate Machines vendor costs** or set a price floor — it's unprofitable everywhere except East.
6. **Double down on the West region** for expansion and marketing spend — the highest return per dollar sold.
7. **Audit Central's Furniture sales** to see if Tables/Bookcases volume explains its region-wide margin compression.

## Dashboard

The Power BI report  includes:

- **KPI cards:** Total Revenue, Total Profit, Profit Margin, AOV, and Basket Size.
- **Filters:** Order Date range, Region, and State.
- **Revenue and Profit Margin by Region:** combo chart (columns + margin overlay).
- **Profit Margin % by Discount Level:** line chart showing the margin cliff past 20% discount.

Styled in dark mode with a navy/cyan two-color palette.


[ARROW STACK PROJECT ANALYSIS.docx](https://github.com/user-attachments/files/32669318/ARROW.STACK.PROJECT.ANALYSIS.docx)
