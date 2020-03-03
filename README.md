# minecraft-add-on-schemas
JSON schemas for Minecraft Bedrock Edition add-on developers

### Usage
These steps are for [Visual Studio Code](https://code.visualstudio.com/)

#### Local to project
1. Create .vscode folder at root of project
2. Create `settings.json` folder
3. Add the following:
```jsonc
    // Allows comments in JSON files
    "files.associations": {
        "*.json": "jsonc"
    },
    "json.schemas": [
        {
            "fileMatch": [
                // Entity behavior files
                "/*.behavior.json",
                "entities/*.json"
            ],
            "url": "https://raw.githubusercontent.com/BlueFrog130/minecraft-add-on-schemas/master/entity.schema.json"
        }
    ]
```
  The `"fileMatch"` option checks the schema against any files ending in `".behavior.json"` or any file within the `entities/` directory
