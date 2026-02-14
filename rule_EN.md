# Basic Rules Tutorial

This section is intended for players encountering Land Battle Chess for the first time, with step-by-step explanations.

# I. Game Objective

Land Battle Chess is a two-player strategic board game. Victory is achieved when one of the following two conditions is met:

- Find and capture the opponent’s **Flag**
- Make the opponent lose the ability to continue fighting through captures or positional blocking (no movable pieces remaining)

# II. Board Structure

## 1. Barracks

- The most common square grids on the board, each can hold a single piece.

## 2. Camps

- Circular grids on the board, 10 in total, each can hold a single piece.
- Pieces in camps **cannot** be attacked, so camps can be used to protect key pieces or occupy strategic positions.

## 3. Railways

- Paths marked with **thick** lines on the board.
- Pieces can move **multiple** grids at once along the railway (unlimited steps, but must follow the track).
  - Most pieces: can only move in a **straight** line along the railway and cannot turn.
  - Engineers: can **turn** freely along railway lines and are the only pieces that can “change direction”.

## 4. Roads

- Paths marked with **thin** lines on the board.

- Pieces can **only** move **one** grid at a time along roads.

# III. Piece Types and Rank Relationships

The core mechanism of Land Battle Chess is that “military rank determines capture relationships”.

From highest to lowest, the pieces are: **Commander-in-Chief, Army Commander, Division Commander, Brigade Commander, Regimental Commander, Battalion Commander, Company Commander, Platoon Leader, Engineer**.

Their corresponding Chinese names are: **司令、军长、师长、旅长、团长、营长、连长、排长、工兵**.

In addition, there are special pieces: **Bomb**, **Landmine**, and **Flag** (**炸弹**、**地雷** and **军旗**).

Capture rules are as follows:

- Higher-ranked pieces can capture lower-ranked pieces
- Pieces of the same rank eliminate each other
- Special pieces follow independent rules (see below)

# IV. Special Pieces

## 1. Engineer

- The only piece that can turn on railways
- Can remove **landmines** without taking damage
- Has the strongest mobility but requires protection

## 2. Bomb

- When encountering any piece, both are eliminated (it can also be intentionally triggered by the opponent’s piece)
- Preferably used to eliminate high-ranked pieces and avoid being wasted on low-ranked ones

## 3. Landmine

- Cannot move
- As long as one side still has landmines on the board, its **Flag** cannot be attacked
- Depending on the rules, there are different ways to eliminate them (described below)

## 4. Flag

- Cannot move
- Being captured results in immediate defeat

# V. Flip Action Rules

This game adopts the “flip mode”, described in detail below.

## 1. Initial State

- All pieces are face down
- Both sides do not know the identities of the pieces

## 2. Action Rules

- Flipping a piece itself counts as one action
- Only after flipping can the piece’s ownership and type be known
- After determining factions, players may operate their own revealed pieces (move or capture), or flip another unknown piece

## 3. Faction Determination

- At the start, only flipping pieces is allowed
- **The player who first flips two pieces of the same color consecutively is assigned to that faction** (this is the implementation in this version; another common rule is to agree on each side’s color before the game begins)
- Movement and attacks can only begin after factions are determined

# VI. Two Sets of Rule Conventions

## Default Rules

### Mine Clearing

Only **Engineers** and **Bombs** can remove **landmines**.

### Capturing the Flag

After all of the opponent’s **landmines** are cleared, any piece may capture the opponent’s **Flag**.

## Optimized Rules

It is not difficult to see that under the default rules above, if all **Engineers** and **Bombs** are eliminated while **landmines** remain uncleared, the game cannot progress and may easily result in a draw. Therefore, the following optimized rules are introduced to enhance competitiveness and intensity. The server can enable the “second rule set” before the game starts.

### Mine Clearing Without Engineers

If all **Engineers** on one side are eliminated, the piece with the **current lowest rank** may be used to eliminate a **landmine** together with itself.

### Restricted Flag Capture Method

The piece with the **current lowest rank** must be used to eliminate itself together with the **Flag** (capture the **Flag**).

# VII. Other Rules in This Game Version

## Action Time Limit

- Each action is limited to 20 seconds (60 seconds in Night Mode)
- Timeout handling:
  - The current turn is considered forfeited
  - The opponent takes the turn
- Accumulating 3 timeouts results in a loss (Night Mode: 1 timeout leads directly to defeat)

# VIII. Beginner Strategy Suggestions

- When your own pieces appear during the flipping phase, prioritize moving them into camps to protect them while securing positional advantages
- Preserve **Engineers** as much as possible for efficient mine clearing when landmines appear in the midgame
- Preserve **Bombs** as much as possible to deter and eliminate high-ranked pieces
- If optimized rules are enabled, try to anticipate the positions of **low-ranked** pieces on both sides; for example, when **Engineers** are about to be eliminated, you may deploy a **Platoon Leader** in advance near the opponent’s **landmines** for preparation, and also guard against similar intentions from the opponent

By mastering the above content, you will be able to complete a full standard-mode Land Battle Chess match. Enjoy the game!