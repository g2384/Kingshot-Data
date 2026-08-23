# Wavebound Voyage

## Unlock slots

| Voyage Slot | Price   | Average Voyage |
| ----------- | ------- | -------------- |
| 1           | 0       | 14             |
| 2           | 1000    | 28             |
| 3           | 10000   | 42             |
| 4           | Unknown | -              |

## Exploration Rewards

| Voyage Count | Rewards          |
| ------------ | ---------------- |
| 1            | 9 Charm Guides   |
| 5            | 18 Charm Guides  |
| 20           | 36 Charm Guides  |
| 60           | 72 Charm Design  |
| 120          | 162 Charm Design |
| 200          | 216 Charm Design |
| 350          | Unknown          |
| 550          | Unknown          |
| 800          | Unknown          |

## Treasures

| Treasure  | Drop rate | Merge Resources | Merge Chance | Item 1          | Item 2          | Item 3          |
| --------- | --------- | --------------- | ------------ | --------------- | --------------- | --------------- |
| Common    | 90%       | -               | -            | 5 Charm Design  | 90m Speedups    | 200 Gems        |
| Premium   | 10%       | 3x Common       | 100%         | 10 Charm Design | 360m Speedups   | 5 Charm Guides  |
| Exquisite | 0%        | 3x Premium      | 75%          | 15 Charm Design | 2 Mystic Shards | 15 Charm Guides |
| Majestic  | 0%        | 3x Premium      | 25%          | 50 Charm Design | 6 Mystic Shards | 50 Charm Guides |

## Best Strategy

### Assumptions

- Each voyage produces one treasure and one exploration count.
- Slot prices are paid at the beginning of the event. The listed voyage counts are cumulative: 14, 28, and 42.
- Treasure drops are independent: 90% Common and 10% Premium.
- Charm Designs, Charm Guides, and Mystic Shards cannot be converted into Gems. Direct Gems are counted separately. Speedups are also separate; `120m Speedups = 1000 Gem-equivalent` is only a comparison rate.
- The fourth slot and milestone rewards above 200 have no usable data.

### Expected treasure rewards

For one treasure:

| Treasure  | Charm Design | Speedups | Direct Gems | Charm Guides | Mystic Shards |
| --------- | ------------ | -------- | ----------- | ------------ | ------------- |
| Common    | 5            | 90m      | 200         | 0            | 0             |
| Premium   | 10           | 360m     | 0           | 5            | 0             |
| Exquisite | 15           | 0        | 0           | 15           | 2             |
| Majestic  | 50           | 0        | 0           | 50           | 6             |

| Reward        | Expected amount per treasure      |
| ------------- | --------------------------------- |
| Charm Designs | `0.90 x 5 + 0.10 x 10 = 5.5`      |
| Speedups      | `0.90 x 90m + 0.10 x 360m = 117m` |
| Direct Gems   | `0.90 x 200 = 180 Gems`           |
| Charm Guides  | `0.10 x 5 = 0.5`                  |

### Milestone rewards

Milestones are cumulative. At the expected voyage counts, the rewards are:

| Total explorations | Milestones reached | Guaranteed milestone rewards    |
| ------------------ | ------------------ | ------------------------------- |
| 14                 | 1, 5               | `9 + 18 = 27 Charm Guides`      |
| 28                 | 1, 5, 20           | `9 + 18 + 36 = 63 Charm Guides` |
| 42                 | 1, 5, 20           | `63 Charm Guides`               |

Slot 2 is especially valuable because it crosses the 20-exploration threshold and adds 36 guaranteed Charm Guides. Slot 3 does not reach a new listed milestone under the current voyage data.

### Merge decision

If Charm Designs are the priority, do not merge:

- `3 Common -> 1 Premium`: 15 Designs become 10 Designs.
- `3 Premium -> Exquisite/Majestic`: 30 Designs become `0.75 x 15 + 0.25 x 50 = 23.75` Designs.

Merge only when Mystic Shards or Charm Guides are more important than Charm Designs.

### Start-of-event slot decision

| Start-of-event choice |  Total cost | Expected voyages | Expected direct Gems earned | Expected Charm Designs | Milestone Guides |
| --------------------- | ----------: | ---------------: | --------------------------: | ---------------------: | ---------------: |
| Slot 1 only           |      0 Gems |               14 |          `14 x 180 = 2,520` |        `14 x 5.5 = 77` |               27 |
| Slots 1-2             |  1,000 Gems |               28 |          `28 x 180 = 5,040` |       `28 x 5.5 = 154` |               63 |
| Slots 1-3             | 11,000 Gems |               42 |          `42 x 180 = 7,560` |       `42 x 5.5 = 231` |               63 |

Net direct Gems after the purchase are:

- Slot 1 only: `2,520 - 0 = 2,520 Gems`
- Slots 1-2: `5,040 - 1,000 = 4,040 Gems`
- Slots 1-3: `7,560 - 11,000 = -3,440 Gems`

**Strategy:** decide at the event start. Choose Slots 1-2 for the best direct-Gem result and the extra 20-exploration milestone. Choose Slot 3 only if 14 additional voyages, 77 additional Charm Designs, and other non-tradable rewards are worth 10,000 Gems. Keep treasures unmerged when Charm Designs are the rarest priority.

