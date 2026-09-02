# Antigua and Barbuda Administrative Divisions / Antigua and Barbuda



## Overview

| Item | Details |
|------|---------|
| Parish | 8 |
| Locality | 117 |
| Coordinates | ✅ Included (all levels) |
| Formats | JSON, NDJSON, CSV |
| License | CC-BY-4.0 |
| Last Updated | 2026-09-02 |
| Website | [openadmindata.org/ag](https://openadmindata.org/ag/) |
| API | [openadmindata.org/api/ag](https://openadmindata.org/api/ag/) |
| Flag | [PNG](https://onlygames.me/flags-png/ag/) · [CDN](https://www.freeflags.org/cdn/) · [CSS](https://www.freeflags.org/css/) · [Collections](https://www.freeflags.org/collections/) |
| National Anthem | [🎵 Listen & Download Antigua and Barbuda National Anthem MP3](https://onlygames.me/national-anthems/ag/) |

## Browse by Parish

| # | Parish | Localitys | Link |
|---|----|----|------|
| 1 | Barbuda | 3 | [Browse](divisions/barbuda-ag01/) |
| 2 | Redonda | 0 | [Browse](divisions/redonda-ag02/) |
| 3 | Saint George | 9 | [Browse](divisions/saint-george-ag03/) |
| 4 | Saint Peter | 14 | [Browse](divisions/saint-peter-ag04/) |
| 5 | Saint Philip | 17 | [Browse](divisions/saint-philip-ag05/) |
| 6 | Saint Paul | 20 | [Browse](divisions/saint-paul-ag06/) |
| 7 | Saint Mary | 24 | [Browse](divisions/saint-mary-ag07/) |
| 8 | Saint John | 30 | [Browse](divisions/saint-john-ag08/) |

## Data Files

| File | Format | Description |
|------|--------|-------------|
| [all-parish.json](data/all-parish.json) | JSON | All 8 parish records |
| [all-locality.json](data/all-locality.json) | JSON | All 117 locality records |
| [all-flat.json](data/all-flat.json) | JSON | Levels 1-1 flat array |
| [all-flat.ndjson](data/all-flat.ndjson) | NDJSON | Streaming format |
| [all-flat.csv](data/all-flat.csv) | CSV | Spreadsheet format |
| [hierarchy.json](data/hierarchy.json) | JSON | Nested tree |
| [schema.json](data/schema.json) | JSON Schema | Data schema |

## Quick Start

### Python

```python
import json

with open("data/all-parish.json", "r", encoding="utf-8") as f:
    data = json.load(f)

for r in data:
    print(f"{r['name']['local']} ({r['name']['en']}) — {r['children_count']['locality']} localitys")
```

### JavaScript

```javascript
import { readFileSync } from "fs";

const data = JSON.parse(readFileSync("data/all-parish.json", "utf-8"));
console.log(`Total: ${data.length} parishs`);
```

## Schema

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Unique identifier |
| `level` | integer | 1=parish, 2=locality |
| `level_name` | object | Level label (local + English) |
| `name.local` | string | Name in local script |
| `name.en` | string | English name |
| `name.slug` | string | URL-safe slug |
| `parent` | object/null | Parent division reference |
| `ancestors` | array | Full ancestor chain |
| `children_count` | object | Count of children per level |
| `zip_codes` | array | Postal codes (where available) |
| `geo.lat` | string | Latitude (WGS84) |
| `geo.lon` | string | Longitude (WGS84) |

Full schema: [data/schema.json](data/schema.json)

## Hierarchy Browse

```
divisions/{parish-slug}/
```

Localitys are listed inline in each parish's README.

## AI Integration

- [llms.txt](docs/llms.txt) — Quick reference for AI agents
- [llms-full.txt](docs/llms-full.txt) — Summary with per-parish links
- [Per-parish data](docs/llms-full/) — Full data by parish

## Citation

```
Antigua and Barbuda Administrative Divisions Dataset (CC-BY-4.0)
URL: https://github.com/open-admin-data/antigua-and-barbuda-administrative-divisions
```

See [CITATION.cff](CITATION.cff) for machine-readable citation.

## License

- **Data**: [CC-BY-4.0](LICENSE)

## Related

- [Open Admin Data](https://openadmindata.org) — Browse, search and explore administrative divisions for every country
- [open-admin-data](https://github.com/open-admin-data) — GitHub organization with all country repos
- [ListBase](https://www.listbase.org) — Structured reference data for every country
- [FreeFlags.org](https://www.freeflags.org) — Free flag images for every country
- [Flag CDN](https://www.freeflags.org/cdn/) — Hotlink flag images directly
- [Flag CSS](https://www.freeflags.org/css/) — CSS flag sprites for web projects
- [Flag Collections](https://www.freeflags.org/collections/) — Curated flag image packs
