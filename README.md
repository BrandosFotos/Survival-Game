## Authors

```text
Halian Hayes
Ethan Peters
Bryan Bosecker
Brandon White
```


# Survival Game

### Purpose
Survival Game is a realistic, text-based wilderness survival game. The player must survive in an unpredictable wilderness by managing limited resources, exploring their surroundings, responding to changing weather, and overcoming environmental and hostile threats.

The game is designed around resource management and decision-making. Players will need to decide when to explore, when to gather resources, when to rest, and how to use the supplies they have available. Different locations, weather conditions, and encounters will create changing situations for the player.

### High-Level Features
- **Foraging** — Search wilderness locations for useful food and natural resources.
- **Fishing** — Fish at suitable locations to obtain food.
- **Random Encounters** — Encounter unpredictable wildlife, environmental hazards, and other events while exploring.
- **Dynamic Weather** — Weather conditions change over time and affect the player's survival.
- **Inventory Management** — Collect, store, and use items while dealing with limited supplies.
- **Crafting** — Combine gathered resources to create useful survival equipment and supplies.
- **Health System** — Track the player's physical condition through hunger, thirst, tiredness, and sickness.
- **Day/Night Cycle** — Time progresses throughout the game and changes the conditions in which the player survives.
- **Illness & Sickness** — Poor conditions and environmental events can negatively affect the player's health.
- **Exploration** — Travel between different wilderness locations to find resources and encounter new situations.

- **High Scores** — Track and display successful survival runs.
- **Save/Load** — Allow players to save their current game and continue it later.

## Data

The game will use JSON data to represent information needed by the survival system. The initial dataset is organized into five main data types:

1. **Items** — Food, water, tools, materials, and other objects the player can collect or use.
2. **Locations** — Wilderness areas the player can explore, including resources and possible encounters.
3. **Weather** — Weather conditions that can affect the player's survival.
4. **Encounters** — Random situations that can occur while exploring.
5. **Creatures** — Wildlife that may be encountered in the wilderness.

The data is stored in the `data` folder as separate JSON files. The dataset contains multiple entries and different values so that the program can support the planned features.

### Example: Items
An item contains information such as its name, category, description, and effects.

```json
{
  "id": "water_bottle",
  "name": "Water Bottle",
  "category": "consumable",
  "description": "A bottle containing drinkable water.",
  "effects": {
    "thirst": 30
  },
  "quantity": 1
}
```

The item data will allow the game to determine what an item is used for and how it affects the player.

### Example: Locations
Locations describe areas that the player can explore.

```json
{
  "id": "pine_forest",
  "name": "Pine Forest",
  "description": "A dense forest containing pine trees, brush, and small streams.",
  "resources": ["berries", "mushroom", "stick", "stone"],
  "encounters": ["deer_sighting", "bear_encounter"],
  "water_available": true
}
```

Locations provide the environment for activities such as exploration and foraging.

### Example: Weather
Weather data describes conditions that can affect survival.

```json
{
  "id": "heavy_rain",
  "name": "Heavy Rain",
  "description": "Continuous heavy rain reduces visibility and makes staying warm more difficult.",
  "effects": {
    "temperature": -7,
    "tiredness": 6,
    "visibility": 45
  }
}
```

### Example: Encounters
Encounters represent random events that can occur during exploration.

```json
{
  "id": "injured_deer",
  "name": "Injured Deer",
  "type": "wildlife",
  "description": "You discover an injured deer nearby.",
  "possible_outcomes": ["leave_the_area", "approach_carefully"]
}
```

### Example: Creatures
Creature data describes wildlife that can be encountered.

```json
{
  "id": "black_bear",
  "name": "Black Bear",
  "behavior": "territorial",
  "danger_level": 5,
  "habitats": ["pine_forest", "mountain_trail"]
}
```

## Initial Dataset Structure

```text
Survival_Game/
├── documentation/
    └── HOWTO.md
└── data/
    ├── items.json
    ├── locations.json
    ├── weather.json
    ├── encounters.json
    └── creatures.json
```

This initial dataset provides the foundation for implementing the planned game features in later iterations. The data can be expanded as additional mechanics are implemented.