# Casting the Maze Spell
Conjures a maze.

## Definition
It is required to have an easy to use Maze Structure Generator, able to provide a representation of a complete maze so that:
- The maze has the number of required entrances.
- The maze has the number of required exits.
- The maze has the number of required halls.
- No area of the maze overlaps the location of another, this is if two or more halls are crosing each other, the crossing area is part of all halls.
- The number of connections of an area are between the expected, for example in a real maze standing in an area you can go north, south, east and west or even also go up or down, or just north.
- The length of a hall is based on the number of areas in it.
- The length of any hall is between the expeted size.

## Representations
To accomplish this we need to model the maze structure:

### An Area
Simplest representation of a space in the maze.
- Knows its location
- Knows that its conencted to other areas (see portals)
- Can be extended to represent special areas like maze entrance or goals, connectons to other mazes, etc.

### Portals
Connect only two areas, representation of doors, gates, etc.
- Contains two area references
- Can be extended to hold status like locked, blocked, etc.
 
### Halls
The collection of areas, representing a type of path where the navegator would start and end.
- Contains a list of areas
- Can be extended to hold

### The Maze
Holding all the data of the inner structures

