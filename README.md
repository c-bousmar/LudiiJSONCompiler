# Compiler from .lud to .json (WIP)
This is a compiler made to create .json files based on .lud files while keeping content integrity.

## TODO parsing
- [x] define
- [ ] game
- [x] option
- [x] rulesets
- [ ] metadata

Game and Metadata are both treated as one simple string for now.

## Structure
```
📂 LudToJsonCompiler/
│── 📂 data/
│   ├── 📂 json/             # Parsed JSON files
│   ├── 📂 processed/        # Cleaned data files
│   ├── 📂 raw/              # Raw input data files
│── 📂 src/
│   ├── clean_files.py
│   ├── fetch_lud_files.py
│   ├── parse_json.py
│── .gitignore
│── poetry.lock              # Locked dependencies for Poetry
│── pyproject.toml           # Poetry configuration file
│── README.md
```

## Usage
If a `"game name"` is given, the script only tries for that specific game, do it for all otherwise.
#### Running everything together:
```shell
python main.py <"game name">
```

#### Fetch `.lud` files:
```shell
python src/fetch_lud_files.py <"game name">
```

#### Clean `.lud` files (because of the format variety introduced by humans) and save in in `.txt` format:
```shell
python src/clean_files.py <"game name">
```

#### Parse cleaned `.txt` format content to `.json`:
```shell
python src/parse_json.py <"game name">
```
