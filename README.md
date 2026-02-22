NarrativeProject
A small text-based adventure game built in C# (.NET Framework 4.8), where you explore rooms, find clues, and escape.
Gameplay
You navigate between rooms by typing the name of an option shown in [brackets]. The goal is to find a key and unlock the door out of your bedroom.
Rooms

Bedroom – Your starting room. Contains a door, a bathroom, and access to the attic.
Bathroom – A clue is hidden here.
Attic – Contains a locked chest that holds the key you need.

How to Win

Go to the bathroom and interact with the mirror to find a code.
Head to the attic and use the code to open the chest and collect the key.
Return to the bedroom and use the door to escape.

Getting Started
Requirements

Visual Studio 2017 or later
.NET Framework 4.8

Running the Game

Clone the repository.
Open NarrativeProject.sln in Visual Studio.
Build and run the project (F5).

Project Structure
NarrativeProject/
├── Program.cs          # Entry point, game loop
├── Game.cs             # Core game logic and room transitions
├── Room.cs             # Abstract base class for all rooms
└── Rooms/
    ├── Bedroom.cs
    ├── Bathroom.cs
    └── AtticRoom.cs
Extending the Game
To add a new room:

Create a new class in the Rooms/ folder that inherits from Room.
Implement CreateDescription() and ReceiveChoice().
Register the room in Program.cs with game.Add(new YourRoom()).
Use Game.Transition<YourRoom>() from other rooms to link to it.
