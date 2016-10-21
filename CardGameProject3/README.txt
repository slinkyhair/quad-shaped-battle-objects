GAME FRAMEWORK:

There are 2 blueprints within the project that will hold the game logic.  The first is the Game Mode blueprint.  This blueprint will
	hold the logic within the game that is unchanging (game rules, game structure, etc.).  Since the game will be multiplayer,
	all of the game logic that changes with the game will be held in the Game State blueprint (player health, cards in hand, etc).
	This is important because the Game Mode blueprint will be held on the server (whichever player is the host) and the Game State
	blueprint will exist separately for each player.

The Player Controller blueprint will hold all of the necessary logic for controlling how each player can interact with the cards and
	environment.  Mostly it will deal with handling user input for card interactions.

The Card blueprint obviously holds all of the card logic and info (card id, value, cost, etc).  There needs to be logic in the Card
	blueprint to dynamically texture the card meshes (we can't have a separate card blueprint for each card type).  I have started
	working on this and have a foundation, but haven't fully implemented it or tested it.

There will be a Deck blueprint for dealing with the deck logic (shuffling and contents basically).  This has not been started.