# inventory-calculator
Free web tool that calculates EOQ, safety stock and reorder point, with an inventory chart.

# Inventory Planning Calculator

A free web tool that tells you how much inventory to order, when to reorder, and how much safety stock to keep.

**Try it here:** https://jltwin.github.io/inventory-calculator/

## Why I built it

I wanted to turn what I'm learning in supply chain courses into something other people can use. Small business owners and students can enter their own numbers and get an ordering plan in seconds, without a spreadsheet.

## What it does

- Calculates economic order quantity (EOQ), safety stock and reorder point
- Updates results live as you type
- Catches blank, zero or negative inputs with a clear message
- Draws an inventory-over-time chart showing when to reorder

## How to use it

1. Enter annual demand, cost per order and holding cost
2. Enter lead time, days open per year and daily demand variability
3. Pick a service level (90%, 95% or 99%)
4. Read the results and the chart

## Formulas

| Result | Formula |
|---|---|
| EOQ | √(2 × D × S ÷ H) |
| Safety stock | Z × σ × √L |
| Reorder point | (d × L) + safety stock |

- **D** = annual demand
- **S** = cost per order
- **H** = holding cost per unit per year
- **Z** = z-score for the service level (1.28, 1.65 or 2.33)
- **σ** = standard deviation of daily demand
- **L** = lead time in days
- **d** = average daily demand (D ÷ days open per year)

## Example

12,000 units a year, $75 per order, $2.50 holding cost, 7-day lead time, 360 days open, daily std. dev. of 8, 95% service level:

- EOQ: **849 units**
- Safety stock: **35 units**
- Reorder point: **268 units**

## Assumptions

- Demand is fairly steady through the year
- Lead time is consistent
- The full order arrives at once
- No bulk discounts

## Built with

- HTML, CSS and JavaScript
- [Chart.js](https://www.chartjs.org/) for the chart
- GitHub Pages for hosting

## Author

Adriana Jaime Lara, BComm student in Operations & Supply Chain Management at the University of Calgary.
LinkedIn: https://www.linkedin.com/in/adriana-jaime-lara-493418238/
