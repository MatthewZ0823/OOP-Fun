# **Pokemon Game - Programming Assignment**
Create a simple turn based game, *inspired* by Pokemon

## Move Class:
- Represents a move that a Pokemon can use
- The Move class will have the following attributes:
    - Name
    - Base Power
- Both the Name and Base Power of the move will be initialized in the constructor
```java
    // Example Move
    Move myMove = new Move("Tackle", 40);
```
- The Move class will have the following methods:
    - `getName`
        - The `getName` method returns the name of the move
    - `getBasePower`
        - The `getBasePower` method returns the base power of the move

## Pokemon Class:
- Represents a Pokemon
- The Pokemon class will have the following attributes:
    - Name
    - Current Health Points
    - Max Health Points
    - Attack Stat
    - Defence Stat
    - Level
    - 2 Moves
- The Name, Max Health Points, Attack Stat, Defence Stat, and 2 Moves will be initialized in the constructor
```java
    // Example Pokemon
    Pokemon myPokemon = new Pokemon("Bulbasaur", 45, 49, 49, move1, move2);
```
- The Level will be a random value from 50 to 100
- A Pokemon's current health points will start at its max health when first constructed, but will change based on the flow of battle

- The Pokemon class will have the following methods:
    - `attack`
        - The `attack` method takes in one parameter (which move to use)
        - The `attack` method then returns how much damage should be dealt to an opposing pokemon
        - *Attack Damage = Move Base Power + Attack Stat + Level*
    - `takeDamage`
        - The `takeDamage` method takes in one parameter (how much damage is dealt to the pokemon)
        - The `takeDamage` method calculates how much health should be lost from current health points
        - *Health Lost = Damage Taken - Defence Stat - Level*

## Battling:
- Create two Pokemon to battle against each other
- The Pokemon alternate turns attacking each other
- On every turn, prompt the user and ask which move they'd like to use
- The battle ends when one Pokemon reaches 0 hitpoints and faints
