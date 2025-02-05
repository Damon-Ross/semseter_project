This program is a simple casino-style slot machine game built using the pygame library in Python. Players can spin the reels, match symbols, and win coins. The game includes adjustable odds for symbol appearances, win messages, and a jackpot feature.

Features

* Spin the Reels:  
* Players can click the lever to spin the reels.  
* Each spin costs 5 coins.

Symbol Matching:

* If all three reels show the same symbol, the player wins coins.  
* Regular wins award 10 coins.  
* Jackpots award 100 coins.

Adjustable Odds:

* The likelihood of each symbol appearing can be adjusted by modifying the symbol\_probabilities dictionary.

Win Messages:

* Temporary messages display when the player wins:  
* "You won 10 coins\!" for regular wins.  
* "JACKPOT\! You won 100 coins\!" for jackpots.

Game Over:

* If the player's balance drops below 0, the game ends.  
* Players can restart the game with a balance of 100 coins.

**How to Play**

Start Screen:

* The game begins on the start screen with instructions.  
* Click the "Start" button to begin.

Main Game:

* Click the lever to spin the reels.  
* Watch the reels spin and stop.  
* If you match three symbols, you win coins.

Game Over:

* If you run out of coins, the game over screen appears.  
* Click "Play Again" to restart.

**Code Structure**  
Constants:

* WIDTH, HEIGHT: Screen dimensions.  
* symbol\_probabilities: Dictionary defining the likelihood of each symbol appearing.

Reel Logic:

* The reel list is generated based on symbol\_probabilities.  
* The reel\_result() function randomly selects a symbol from the reel.

Game Screens:

* draw\_start\_screen(): Displays the start screen with instructions.  
* draw\_game\_over\_screen(): Displays the game over screen.

Win Logic:

* When all reels stop, the program checks if they match.  
* If they match, the player wins coins, and a win message is displayed.

Main Game Loop:

* Handles user input, updates the game state, and renders the screen.

**Customization**  
Adjusting Odds:

* Modify the symbol\_probabilities dictionary to change how often symbols appear.

Example:

symbol\_probabilities \= {  
    'cherry': 10,  \# Very likely  
    'melon': 4,  
    'lemon': 3,  
    'apple': 2,  
    'star': 1,  
    'jackpot': 0.5,  \# Extremely rare  
}  
Changing Rewards:

Modify the reward amounts in the win logic:

python  
Copy  
if symbol \== 'jackpot':  
    balance \+= 100  \# Jackpot reward  
else:  
    balance \+= 10   \# Regular reward

Win Message Duration:

* Change the duration of the win message by modifying the win\_message\_time calculation:

win\_message\_time \= pygame.time.get\_ticks() \+ 3000  \# 3 seconds

**Dependencies**

* Python 3.x  
* Pygame:

**Known Issues**

* The reel animation is basic and could be enhanced for a smoother experience.  
* The reels sometimes do not align

**Future Improvements**  
Advanced Graphics:

* Improve the reel animation and add sound effects.

Create Algorithm:

* Implement an algorithm that can simulate more closely how real slot machines behave  
* Make it win a lot at first, then slowly make the money go down

