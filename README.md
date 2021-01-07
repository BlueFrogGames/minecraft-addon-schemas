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
    // Schema associations
    // Based on Vanilla reference folder structure
    "json.schemas": [
        {
            "fileMatch": [
                // Entity behavior files
                "/behaviors/entities/*.json"
            ],
            "url": "https://raw.githubusercontent.com/BlueFrog130/minecraft-add-on-schemas/master/entity.schema.json"
        },
        {
            "fileMatch": [
                // Entity resource files
                "/resources/entity/*.json"
            ],
            "url": "https://raw.githubusercontent.com/BlueFrog130/minecraft-add-on-schemas/master/client_entity.schema.json"
        },
        {
            // Spawn rules
            "fileMatch": [
                "/behaviors/spawn_rules/*.json"
            ],
            "url": "https://raw.githubusercontent.com/BlueFrog130/minecraft-add-on-schemas/master/spawn_rules.schema.json"
        },
        {
            // Items
            "fileMatch": [
                "/behaviors/items/*.json"
            ],
            "url": "https://raw.githubusercontent.com/BlueFrog130/minecraft-add-on-schemas/master/item.schema.json"
        }
    ]
```
  The `"fileMatch"` option checks the schema against any files ending in `".behavior.json"` or any file within the `entities/` directory

For more details, or a reference, see the `settings.json` in the [example](https://github.com/BlueFrog130/minecraft-add-on-schemas/blob/master/example/.vscode/settings.json)