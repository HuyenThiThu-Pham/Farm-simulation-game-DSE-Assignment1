## Overview

This project is a farm simulation game built in Java, where players manage a virtual farm by planting crops, harvesting food, and handling in-game events. The game follows an object-oriented structure with different item types, a dynamic field, and a farm economy system.

## Key Features

### 1. Items Package
The game includes different items that interact within the farm:

- Item (Base Class): Tracks age, maturation age, death age, and value. Provides methods to age, check maturity, and return monetary value.
- Food (Abstract Class): Cannot be instantiated but serves as a base for farm produce.
- Grain: Represented as "g" (young) and "G" (mature). Matures in 2 days, dies in 6 days, and is worth $2.
- Apple: Represented as "a" (young) and "A" (mature). Matures in 3 days, dies in 5 days, and is worth $3.
- Weed: Never dies, has a value of -1, and is represented by "#".
- Untilled Soil & Soil: Permanent land representations with different characteristics.
### 2. Field Management
The Field class represents a farm grid where players plant and manage crops. It provides methods to:

- Advance Time: Each item ages per turn; Soil may randomly turn into Weeds.
- Plant Crops: Players can plant Apples or Grain in Soil.
- Harvest Crops: If mature, crops can be harvested for money.
- Till Soil: Converts land to prepare for planting.
- Generate a Summary: Shows item quantities and total farm value.
### 3. Farm System
The Farm class manages gameplay, tracking the field state and the player's bank balance. Players interact through commands:

- t x y → Till soil at (x, y).
- h x y → Harvest mature crops at (x, y).
- p x y → Plant a crop (Apple or Grain) at (x, y).
- s → Display field summary.
- w → Skip turn (aging progresses).
- q → Quit game.
### 4. Custom Feature Extension
This project includes an original new functionality beyond the base requirements, adding depth and strategy to the game. 
