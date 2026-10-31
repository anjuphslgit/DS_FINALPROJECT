# The Dungeon Conquest (TDC)

A text-based dungeon battle game for the Data Structures Laboratory. It uses:
**queue** (Encounter Queue),
**stack** (Battle Action History),
**graph** (the dungeon map of rooms and passages)

## How to run

```bash
python3 DS_FinalProject_MercadoRBanaybanayJBariteJDomingoJGonzalesA.py
```

Run it from this folder so it uses the `.txt` record files here. If a file is
missing, the game recreates it with the default records.

## Default login

| Role  | Username | Password   |
|-------|----------|------------|
| Admin | `admin`  | `admin123` | For admin default account
| Player| `player` | `player123`| For player default account


## Sections for Admins

- **Dashboard**: live totals for players, enemies, battles and boss progress.
- **Profiling**: add, view, search, update and delete players, enemies, items,
  rooms, passages and challenge questions.
- **Transactions**: the player's dungeon expedition (queue enemies, battle,
  shop, rest, escape) and the admin's game setup tools.
- **Report Generation**: nine reports, each exportable to the `reports/` folder.

## Data structures

| Structure | Where it is used | Operations |
|-----------|------------------|------------|
| Queue | Encounter Queue of enemies to fight | enqueue, dequeue, peek, display, empty check |
| Stack | Battle Action History | push, pop (remove latest log entry), peek, display, empty check |
| Graph | Dungeon map: rooms are vertices, passages are two-way edges | add/remove passage, BFS shortest route, DFS traversal, reachability |

## Record files

| File                   | Contents                                |
|------------------------|-----------------------------------------|
| `1player_accounts.txt` | accounts, stats, inventory, saved queue |
| `2enemy_records.txt`   | enemies and the room each one guards    |
| `3item_records.txt`    | shop items and their effects            |
| `4room_records.txt`    | dungeon rooms (graph vertices)          |
| `5room_connections.txt`| passages between rooms (graph edges)    |
| `6question_records.txt`| challenge questions                     |

The game also creates the following while u play:
`battle_history_records.txt`,
`dungeon_game_records.txt`,
`battle_activity_log.txt`
