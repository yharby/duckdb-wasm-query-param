# DuckDB Shell URL Generator

A simple, responsive web tool to generate shareable DuckDB shell URLs with encoded SQL queries. Designed with DuckDB's official brand colors and design guidelines.

## Features

- **URL Encoding**: Encode SQL queries using DuckDB shell's custom encoding scheme
- **Quick Actions**: Copy generated URLs to clipboard or open directly in DuckDB shell
- **Query History**: Automatically saves your last 10 queries in browser localStorage
  - Swipeable cards showing query and timestamp
  - Click any card to reload the query
  - Delete individual queries or clear all history
  - SQL keyword highlighting in history cards
- **Keyboard Shortcuts**: Press Ctrl/Cmd + Enter to generate URL
- **Pre-loaded Example**: Default query included to get started quickly
- **Proper Attribution**: Trademark attribution following DuckDB guidelines

## How It Works

The tool implements DuckDB shell's encoding scheme:
1. Applies custom character swaps (spaces ↔ hyphens, semicolons ↔ tildes)
2. URL encodes the result
3. Generates URLs in format: `https://shell.duckdb.org/#queries=v0,{encoded_sql}`

## Usage

1. Enter your SQL query in the text area
2. Click "Generate URL" (or press Ctrl/Cmd + Enter)
3. Copy the URL or open it directly in DuckDB shell


## Example

Input:
```sql
SELECT * FROM generate_series(1, 10) AS t(id);
```

Output:
```
https://shell.duckdb.org/#queries=v0,SELECT-*-FROM-generate_series(1%2C-10)-AS-t(id)~
```

## Design

This tool follows DuckDB's official brand guidelines in dark mode:
- **Primary Color**: DuckDB Yellow (#FFF100)
- **Dark Theme**: Dark background (#0a0a0a) with dark UI elements
- **Syntax Highlighting**: Orange keywords, purple functions, green numbers, blue strings
- Clean, geometric design with rounded corners
- Accessible color contrast ratios (WCAG AA compliant)

Design guidelines: https://duckdb.org/design/

## Trademark Notice

DuckDB is a registered trademark of the DuckDB Foundation. This is an independent tool that generates URLs for the official DuckDB shell. It is not affiliated with or endorsed by the DuckDB Foundation.

For DuckDB trademark guidelines, visit: https://duckdb.org/trademark_guidelines

## License

MIT
