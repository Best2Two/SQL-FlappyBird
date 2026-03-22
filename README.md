# Flappy Bird SQL Game

A Flappy Bird game implemented entirely in SQL Server.

## How It Works

The game follows a 2-step cycle for each component:

1. **Process**: Each frame, process procedures update the manifest tables by calculating new positions, applying physics, and handling game logic.

2. **Render**: Rendering procedures read from the manifest tables and update the display table using SQL UPDATE statements.

This architecture allows the entire game loop to run within SQL Server without external game engines.

## Setup

**Option 1:**
Create a database named `db_flappy_bird_game` in MS SQL Server.

**Option 2:**
Set up your own `connectivity.py` configuration.

## Installation Steps

1. Run `Tables.sql` to create all required tables.

2. Run all scripts in the `Modules` folder in any order:
   - FrontFrame.sql
   - Processors.sql
   - Rendering.sql

3. Run Populating.sql to create the procedure that will populate the game data by running:
   - Populating.sql

4. Create the initialization procedure by running
   - Initialize.sql

5. Run the game:
   ```
   python connectivity.py
   ```
## Controls

Press spacebar to make the bird jump.

___ 
Everything you see here is literally a table and some queries on it. SQL is fun, **but I really like data because she likes data.**

<p align="center">
  <img src="view.gif" alt="Gameplay">
</p>
