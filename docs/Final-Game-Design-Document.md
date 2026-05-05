Design Document (GDD) Template:
Game Name:
Flour and Fury
Genre: Light strategy, cozy casual, competitive tournament, chance-based
Game Elements:
The player moves around a 17-square space game board by rolling a dice and landing on a space that secures ingredients or triggers event cards (red - mishaps, green- upgrades/boosts). The goal is to build cakes and earn as many points in order to win. The main fun game element involves collecting unique ingredients and choosing which ingredients to bake in your oven slots. 
Player:
2 players, 1v1, 
Technical Specs
Technical Form:
2D Graphics (flat)
View:
Top view; top-down view of the game board for clear visibility of board, color-coded cards, slots, and game pieces (players’ characters)
Platform:
PC
Language:
C#
Device:
PC 
Gameplayer:
# Gameplay
In Flour & Fury, two players are competing as bakers in a competitive baking district for the baking champion title where they each take turns rolling a dice and moving around a 16-tile/space board with assigned ingredients they must collect, match, and bake for additional points. Landing on a normal tile grants the player a random ingredient of each of the following: egg, flour, sugar, and or a sweetner/flavoring. Players must place their ingredient of choice into the oven-baking system consistent of 3-ingredients trays or spaces to place each ingredient in; completion of 5 cakes triggers the end of the game but total number of points accumulated results in a win. 
Some tiles can either boost/upgrade or downgrade either opponent. The green tiles boost the player with additional ingredients for example while the red tiles resilt in losing a turn or an ingredient. Special ingredients are flavors/sweetners that can replace a sugar ingredient in a 3-cake tray system earning the player additional points but the trays are locked once a cake is completed by placing designated ingredients. The red and green tiles are evenly distributed (2-4 red and green cards each equally distributed). 
Gameplay Outline:
Opening: 
Large text display of the rules with a background layer where players can click to confirm anywhere and proceed to play. Clear color-coded game board with a roll button, display of each player’s turn, and small ingredient inventory and image to reference. 
Game Options:
Standard 2-player/multiplayer game still in development with additional or updated UI keys and buttons to direct user to restart/replay, see collected ingredients, and display of oven-baking system. 
Story Synopsis:
Competitive board game set in a Baking District where players are bakers competing to bake cakes to earn points.
Modes:
single competitive 2-player mode (multiplayer), same difficulty
Game Elements:
Rolling Dice, Gameboard tile movement, Ingredient collection, Boosts/mishap tiles, oven-baking cake system, turn-based
Game Levels:
a 16-tile board game in a square path (1x)
Player Controls:
Players roll a dice with a roll button automating movement across gameboard;
Players control ingredient movement and placement into oven-baking cake system;
Winning
The player with the most points accumulated wins. Players accumulate points by building a cake - placing three ingredients (2x bases, 1x sweetner) in the oven-baking tray system.
Losing
The player with fewer points loses. A player accumulating fewer points from lack of special ingredients or cake placement before the other opponent completes all 5 cake slots results in a loss.
End
Players complete all 5 cakes in the oven-baking system by placing three ingredients (2x bases, 1x sweetner) in the oven-baking cake tray.
Why is this fun?
Simple, cozy game features allow players to collect and decide on which cake to bake for the most points before ending the game. It’s a competitive, light strategy made for a broader age demographic from 13+.
Key Features:
Competitive light strategy game
Cozy game features (cake building, rolling dice, collecting ingredients)
Red Mishaps and Green Boost cards 
Special ingredient cards - ingredient card deck
Final-turn rule (completing 5 cakes allows the other play to place final cake with  ingredients available)
Cake-based color palette and appeal
Design Document:
Design Guidelines
The game aims to be a simple and straightforward cozy game with light strategy and chance-based elements. The rules are simple and the gameboard’s design should be made clear with special cards distinguished by colors. If possible, limit the number of red and green cards or possible outcomes so as to not overcome them with too many rules and automated movements. Main goal is to be able to move around the square-shaped board and be able to collect and place ingredients with a clear layout
Game Design Definitions:
Core gameplay:
Collect as many special ingredients and bake cakes with a 3-ingredient cake-system. 
# How the player wins, loses
Opponent with the most points accumulated wins, Opponent with fewer points loses depending on total cake ingredient combinations and point accumulation.
Endgame Trigger:
Player that fills all five cake trays triggers the end of the game where the player with the most points accumulated wins. 
Player Choice:
1. Complete a cake with 3 ingredients 
OR
2. Keep ingredients for a better combination to score more points
 Anti hoarding: Hand Limit Rule
Players can’t hold more than 6 cards at a time, including 2 sweetners/flavors in their collected ingredient deck
Game Flowchart:
Start Up:
board loads, game overview/rules display card (click anywhere to start), Red and green tiles distributed evenly (random placement upon each game restart), Ingredients mark 
Player Turn:
Player “#” turn display appears
Dice result generates upon each player’s turn
Movement automated
Tile:
Start Tile: No effect
Ingredient: Draw random ingredient (ie. flour, eggs, and sugar or sweetener/flavoring)
Red: Red Cards: + Mishaps
Boost cards: positive effects
1: Spilled Milk/Expired Ingredient - Lose 1 Ingredient or last card drawn (common)
2: Missing Ingredient - Skip Turn, no ingredient drawn (common)
3: Kitchen Mix-Up: opponent chooses 1 Ingredient from your collected ingredients deck - (rare)
Green:	•	Boost cards: positive effects
1: Lucky Find - Draw Additional Ingredient Card; Total: 2 Cards (common)
2: Recipe Inspiration - Take last retrieved ingredient from opponent (common)
3: Perfect Timing - Move Roll Again (rare)
Updated UI text:
TextMeshPro display of player’s turn. (ie. “Player 1’s turn” “Player 2’s turn”)
Update turn event
Cake completion
Press and collect ingredients. 
Cake score display, points added
Game Over:
Game ends
Player Winner: “Player1/2 Wins “ Display card
Points Total Display
Player Definitions/Properties:
Player 1/2: PLayers are bakers competing for winner baking champion of the baking district
Ingredients:
Cake System: Each cake requires 3 ingredients for the cake trays( Base: Flour and eggs, Flavoring/sweetner: Sugar or Special Ingredient). 
Special Ingredients: 
1. Chocolate Fudge cake(7 pts), 
2. Blueberry Cheesecake(8 pts), 
3. Strawberry Cheesecake(8 pts), 
4. Tiramisu(9 pts), 
5. Molten Lava Cake(9 pts) points based on rarity and uniqueness; 
Common cakes = fewer points (7 points)
Unique cakes = more points (8-9)
5 Points: Flour, Eggs, Sweetner
7-9 Points: Flour, Eggs, Special Flavor
Ingredient Inventory UI:
Display of all ingredients within each player’s ingredient cards deck
Oven cake baking tray system (empty/open)
User Interface:
Roll Button - Available for each player’s turn, roll once a turn, 
Player Turn Display - (TextMeshPro) visible display of each player’s turn
Player 1 Inventory, Player 2 inventory
3-square grid (1x3) for cakes (X3-5)
Ingredients collection: number count display of ingredients
Change Log
Change 1:
Original Physical Prototype Concept (Design Treatment):
Original version included two phases of the game where reaching the end of the first game board phase (25 tiles originally - formed in a turn spiral style layout) transitioned to the ingredient mixing/allocation phase where players would gather all their collected ingredient cards, then place them in the baking tray system where they’d decide on the final winners based on rare ingredient combinations. 
Feedback:
suggested that the two phases could be merged for easier gameplay without separating game phases, allowing the player to play as they place ingredients in the baking tray.
Improved pacing and simplified game mechanics
Change 2:
Originally left at the end as the game ending triggered after a player completes five cakes allowing the other player to play their last turn as a final attempt of gaining points.
Feedback:
Allow the other player or opponent to place their last ingredients with the given ingredient cards remaining, as a result, increasing the opponent's chances of winning after the player ends the game (increase stakes/risks). 
Change 3:
Simplified and reduced boost/mishap cards (green and red cards) by getting rid of tile placement movements and redundant additional/loss in cards
Result: 
Less redundant impacts, less complicated results with overall simpler gameplay. 
Change 4:
Reduced number of cake trays (1x3) for cake combination results for digital prototype. 
Result: 
Faster gameplay, shorter rounds, takes up less screen space with smaller, more manageable inventory (UI) and ingredient deck. 


