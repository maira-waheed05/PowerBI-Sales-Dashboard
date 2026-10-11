# Amazon Sales Analysis Dashboard

A Power BI report template for exploring Amazon product and sales-related data. The project is provided as a Power BI Template (`.pbit`) and includes a data model, date tables, and DAX measures for year-to-date and quarter-to-date analysis.

## Project Overview

This dashboard is designed to help users analyze product categories, product descriptions, prices, review volumes, shipment information, and order dates. It can be used as a starting point for product and sales reporting in Power BI.

> **Note:** The uploaded project is a `.pbit` template, not a populated `.pbix` report. A template generally requires you to connect or provide the source data when opening it. The actual visuals and results depend on the data source configured for your copy.

## Data Model

### `Amazon_Data`

| Field | Description |
|---|---|
| `Product Category` | Product category |
| `Product Description` | Product description |
| `Price(Dollar)` | Product price/value in dollars |
| `Number of  reviews` | Number of reviews associated with the record |
| `Shipment` | Shipment-related field |
| `Order Date` | Date associated with the order |

The model also contains date-related tables, including `Date Table`, to support time-based analysis.

## Included DAX Measures

| Measure | Definition / Purpose |
|---|---|
| `YTD sales` | Year-to-date sum of `Price(Dollar)` |
| `QTD sales` | Quarter-to-date sum of `Price(Dollar)` |
| `YTD Products Sales` | Year-to-date count of product-category records |
| `YTD Reviews` | Year-to-date sum of review counts |

These measures use the `Date Table[Date]` field for time intelligence. Verify the relationship between the date table and `Amazon_Data[Order Date]`, and ensure the date table covers the relevant reporting period, before relying on time-based results.
