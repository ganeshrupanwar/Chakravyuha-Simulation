# Chakravyuha Simulation

This repository contains a Python implementation for simulating and visualizing the Chakravyuha scenario. The code determines whether a player can cross a series of enemy encounters while managing power, skips, and recharges.

## Problem Statement

The player needs to navigate through a series of enemy encounters arranged in a circular formation, simulating the Chakravyuha. The player starts with a certain amount of power and can skip or recharge their power a limited number of times. Some enemies have regenerating power, which affects the player's power during encounters.

## Function Description

The function can_cross_chakravyuha(p, enemies, a, b) simulates the scenario and provides visual outputs of the player's power levels through the encounters.

### Parameters

- `p` (int): The initial power of the player.
- `enemies` (list of int): A list containing the power levels of enemies in each encounter.
- `a` (int): The number of times the player can skip fighting an enemy.
- `b` (int): The number of times the player can recharge their power.

### Returns

tuple: A tuple containing:

- `bool`:Indicates if the player can cross all encounters successfully.
- `power_levels`(list of float): List of power levels after each encounter.
- `events`(list of str): List of events that occurred during the simulation.

### Logic

1. **Initial Setup**: Initialize the player's power, available skips, and recharges.
2. **Loop Through Circles**: Iterate through each level and apply the following rules:
   - Handle regenerating enemies by adjusting power.
   - Skip encounters if skips are remaining.
   - Recharge power if recharges are available and current power is insufficient.
   - Check if the player’s power is below the enemy’s power and return False if so.
   - Deduct the enemy’s power from the player’s power.
3. **Final Check**: Return True if the player successfully crosses all encounters.


### Example Test Case 1

- Initial power: 9
- Enemies: [1, 1, 1, 2, 2, 2, 5, 5, 8, 2, 3, 1]
- Skips: 3
- Recharges: 2

### Example Test Case 2

- Initial power: 15
- Enemies: [5, 6, 8, 7, 10, 3, 9, 6, 7, 8, 7]
- Skips: 3
- Recharges: 2

## Visualization

**The simulation generates two plots:**:

- **Circular Plot:** Represents the power levels around the circular Chakravyuha formation. Each layer (or circle) corresponds to an encounter, with annotations for events.

- **Step-by-Step Plot:** A linear plot showing power levels after each enemy encounter with annotations for each event.

## Running the Code

To run the code, execute the Python script in a Python 3 environment. The code uses Matplotlib for plotting and requires numpy for numerical operations. Modify the test cases as needed to explore different scenarios.

