Battleship Game - Readme File
A complete desktop-based implementation of the classic Battleship game built using JavaFX, with support for multiplayer via sockets, drag-and-drop ship placement, AI testing, real-time feedback, and JUnit test coverage.
________________________________________
Table of Contents
●	Features
●	How to Run
●	Technologies Used
●	Gameplay Overview
●	Architecture
●	Testing
●	Screenshots (Optional)
●	Future Enhancements
●	License
________________________________________
Features
●	Drag and Drop ship placement on a 10x10 grid
●	Ship rotation before placement
●	Interactive error popups using custom ErrorBox
●	Save and Load game state
●	Multiplayer support via socket (Client/Server)
●	AI functionality for positioning logic (testable)
●	IP-based LAN connection between two players
●	Real-time timer, move counter, and scoring system
●	Utility tools like ShipManipulator, MouseGestures for clean MVC-like separation
________________________________________
How to Run
Prerequisites:
●	Java JDK 8+
●	JavaFX SDK 
________________________________________
Technologies Used
●	Java 8
●	JavaFX (Scene, Stage, GridPane, Event handling, Media)
●	Java Sockets (Client/Server communication)
●	Serializable objects (game state)
●	JUnit 4 (for game logic testing)
________________________________________
Gameplay Overview
●	Ship Types:

○	Carrier (5 blocks)
○	Battleship (4 blocks)
○	Cruiser (3 blocks)
○	Submarine (2 blocks)
○	Destroyer (1 block)
●	Setup:

○	Each player places 5 ships using the drag-and-drop UI.
○	Ships can be rotated before placement.
○	Once placed, a player clicks "Play" to finalize their setup.
○	Both players roll a dice to determine who starts.
●	Game Loop:

○	Click a cell in the top grid to fire.
○	Cells change color depending on hit/miss.
○	Popup notifications inform about hits, misses, and sinks.
○	Game ends when one player sinks all ships.
________________________________________
Architecture
.
├── appGame
│   ├── GameGUI.java         # Main UI and launcher
│   ├── GameHelper.java      # Turn logic, communication, game state
│   ├── GameClient.java      # Client-side multiplayer logic
│   ├── GameServer.java      # Server-side multiplayer logic
│   ├── BattleShipMain.java  # Utility and score logic
│   ├── ErrorBox.java        # UI popups
│   ├── Grid Classes         # BottomGrid.java, TopGrid.java
│   ├── Ship Classes         # Carrier, Battleship, Cruiser, Submarine, Destroyer
│   ├── MouseGestures.java   # Ship drag/rotate logic
│   ├── ShipManipulator.java # Ship tracking/rotation state
│   └── IpBox.java           # Multiplayer IP entry modal
└── JUnit
    └── Test4.java           # JUnit tests for gameplay logic

________________________________________
Testing
●	Test Class: JUnit/Test4.java
●	50+ JUnit test cases cover:
○	Score calculation
○	Timer checks
○	AI coordinate logic
○	Game win/loss validation
○	Ship drop state validation
○	Orientation (horizontal/vertical) checks
○	Multiplayer connection validation
________________________________________
Author: Zino

________________________________________

