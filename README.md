# Arc Raiders Tracker Data

Game item database for the Arc Raiders Item Tracker iOS app.

## Automatic Updates

Data is **automatically updated daily** via GitHub Actions:
- Fetches latest data from [RaidTheory](https://github.com/RaidTheory/arcraiders-data)
- Transforms and builds reverse recycling lookup
- Commits changes only if data has changed
- App automatically picks up updates on next launch

### Manual Trigger
Go to **Actions** → **Update Game Data** → **Run workflow**

## Files

| File | Description |
|------|-------------|
| `version.json` | Version metadata (checked by app) |
| `items.json` | Full item database (~495 items) |

## URLs

```
https://raw.githubusercontent.com/aivars/arc-raiders-tracker-data/main/version.json
https://raw.githubusercontent.com/aivars/arc-raiders-tracker-data/main/items.json
```

## Data Source

- **RaidTheory** - https://github.com/RaidTheory/arcraiders-data (MIT License)
- **MetaForge** - https://metaforge.app

## version.json Format
```json
{
  "version": "1.0",
  "updatedAt": "2026-01-14T12:00:00Z",
  "itemCount": 495
}
```
