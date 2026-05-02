# Endfield Development Skills

This repository contains tools and documentation for researching Arknights Endfields game data structures and assets.

## Find Endfield Data

A skill for searching and retrieving game data from Endfields.

### Tables API

Access game data structures via the following endpoints:

| Endpoint | Description |
|----------|-------------|
| `https://endfield-assets.fffdan.com/vfs/Table/` | Get all available table names |
| `https://endfield-assets.fffdan.com/table/{TableName}` | Get keys for a specific table |
| `https://endfield-assets.fffdan.com/table/{TableName}/{Key}` | Get a specific value |
| `https://endfield-assets.fffdan.com/table/{TableName}/all` | Get all values from a table |

### Game Assets

Search and download game resources:

- **Search**: `https://endfield-assets.fffdan.com/vfs/Bundle/search/{query}`
- **Download**: `https://endfield-assets.fffdan.com/vfs/Bundle/file/{path}`

Available asset formats: `.png`, `.tga`