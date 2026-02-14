# Night Mode Rules

Night Mode is an experimental entertainment mode, created as a playful and creative extension by the developer.

Its inspiration comes from *Plants vs. Zombies*.

At the start of a Night Mode match, several pieces will be randomly granted special traits in addition to their default abilities:

1. One **Regimental Commander** — **“Scaredy”**:
   If there is any enemy movable piece adjacent to it, it becomes a **Platoon Leader**; otherwise, it becomes a **Army Commander**.

2. One **Division Commander** — **“Fume”**:
   All roads are treated as railways. If multiple capturable enemy pieces lie along the same straight line (excluding camps) with no blocking pieces in between, it may capture them consecutively in a single action by passing through each one. The final position may be an empty grid, and it may eliminate itself together with the last target, too.

3. One **Commander-in-Chief** — **“Ice”**:
   When revealed, the opponent skips one turn. When it is eliminated, your side skips one turn.

4. One **Bomb** — **“Doom”**:
   The grid where it dies becomes unable to be occupied by any other piece (but still passable).

5. One **random** piece — **“Plantern”**:
   When revealed, all unknown pieces adjacent to it are also revealed. The player controlling this piece can see the identities of adjacent unrevealed pieces.

6. One **random** piece — **“Hypno”**:
   When it captures an enemy piece, it does not move into that grid; instead, the captured piece is converted to your side. When this piece is eliminated, the piece that eliminated it gains the “Hypno” ability.

**The server can configure the types and quantities of these special pieces.**

Night Mode uses **the second rule set** by default, and the time limit per action is extended to 60 seconds. A single timeout results in an immediate loss.