# CES 2026 Exhibitor Database

Comprehensive exhibitor information from CES 2026 (Consumer Electronics Show) including company details, booth locations, product categories, and funding information.

## Access the Database

**[View CES 2026 Exhibitor Database on Google Sheets](https://docs.google.com/spreadsheets/d/1p2KgnD3UI4qH8G3q0rD_hbdEfq480B-j/edit?usp=sharing&ouid=104753634455432639165&rtpof=true&sd=true)**

Download options available in the `output/` directory:
- **JSON**: `CES 2026 Exhibitor Database (Enriched with Funding & Revenue Data).json`
- **CSV**: `CES 2026 Exhibitor Database (Enriched with Funding & Revenue Data).csv`

## Key Insights

This database provides valuable insights for:

- **Investors & VCs**: Identify startups seeking funding, filter by investment stage (Seed, Series A/B/C), funding amounts, and revenue ranges
- **Business Development**: Find potential partners by product category, booth location, and company size
- **Market Research**: Analyze technology trends across AI, robotics, smart home, healthcare, and other innovation sectors
- **Event Planning**: Navigate CES 2026 efficiently with venue locations, booth numbers, and hall assignments
- **Competitive Analysis**: Research companies by category, geography, and funding status

## Database Fields

| Field | Description |
|-------|-------------|
| `name` | Company/exhibitor name |
| `exhid` | Unique exhibitor ID |
| `detail_url` | Link to exhibitor detail page |
| `booth_venue` | Venue location (LVCC, Venetian, etc.) |
| `booth_number` | Booth number |
| `booth_full` | Complete booth location string |
| `description` | Company description |
| `website` | Company website URL |
| `address` | Full company address |
| `product_categories` | Product categories (semicolon-separated) |
| `hall_ids` | Hall location IDs |
| `seek_funding` | Whether seeking investment |
| `funding_amount` | Funding amount sought |
| `revenue` | Company revenue range |
| `investment_stage` | Current investment stage |
| `country` | Company headquarters country |

## Use Cases

### For Investors
Filter companies by:
- `seek_funding = Yes` to find investment opportunities
- `investment_stage` to match your fund's focus (Seed, Series A, etc.)
- `funding_amount` to find deals in your target range
- `revenue` to assess company maturity

### For Business Development
Search by:
- `product_categories` to find companies in your target market
- `booth_venue` and `booth_number` to plan meetings at CES
- `country` to find international partnership opportunities

### For Market Research
Analyze:
- Distribution of companies across product categories
- Geographic representation by country
- Funding landscape and investment trends
- Technology sector breakdowns

---

## Data Collection Tool

This repository also includes the Rust-based scraper used to collect the data.

### Prerequisites

- Rust 1.70+ (install via [rustup](https://rustup.rs/))

### Running the Scraper

```bash
git clone https://github.com/aezizhu/ces_2026_rust_scraper.git
cd ces_2026_rust_scraper
cargo run --release
```

### Technical Details

- **Fast API-based scraping**: Uses the official CES exhibitor API
- **Concurrent requests**: 30 simultaneous connections for speed
- **Dual output formats**: JSON and CSV exports
- **Deduplication**: Automatic removal of duplicates

---

## License

This project is licensed under the **Apache License 2.0** - see the [LICENSE](LICENSE) file for details.

### Attribution Requirements

**If you use this data or software, you MUST provide attribution to the original author.**

```
CES 2026 Exhibitor Database by aezizhu
Licensed under the Apache License 2.0
https://github.com/aezizhu/ces_2026_rust_scraper
```

## Legal Disclaimer

This data is provided for educational and research purposes only. Users are responsible for ensuring compliance with applicable data protection regulations.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## Acknowledgments

- CES (Consumer Electronics Show) for providing the exhibitor platform
