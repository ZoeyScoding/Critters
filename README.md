While it is running the simulation will look something like this:

![image](https://github.com/ZoeyScoding/Critters/assets/137151740/50b68022-cf8b-4136-8d15-5490d29df96e)

The basic behavior of every animal is:

   *Orca*
      - Constructor: public Orca()
      - getColor: Returns the color black when the Orca is hungry, return the color white when it's not hungry.
      - toString: Displays "~~~" when the Orca is hungry and "OOOOO" when it's not hungry.
      - getMove:  The Orca always infects if there's an enemy in front.
                  If the front is empty, it hops.
                  If there's an enemy on the right, it turns right.
                  If there's an enemy on the left, it turns left.
                  Otherwise, it turns left (rotate 90 degrees counter-clockwise) as the default action

   *Lion*
      - Constructor: public Lion()
      - getColor: Randomly picks one of three colors (Color.RED, Color.GREEN, Color.BLUE) 
                  and uses that color for three moves, then randomly picks one of those colors 
                  again for the next three moves, then randomly picks another one of those colors 
                  for the next three moves, and so on.
      - toString: "L"
      - getMove:  always infect if an enemy is in front
                  otherwise if a wall is in front or to the right, then turn left
                  otherwise if a fellow Lion is in front, then turn right
                  otherwise hop.

   *Giant*
      - Constructor: public Giant()
      - getColor: Color.GRAY
      - toString: "fee" for 6 moves, then "fie" for 6 moves, then "foe" for 6 moves, 
                  then "fum" for 6 moves, then repeat.
      - getMove:  always infect if an enemy is in front
                  otherwise hop if possible
                  otherwise turn right.

   *Bear*
      - Constructor: public Bear(boolean polar)
      - getColor: Color.WHITE for a polar bear (when polar is true),
                  Color.Black otherwise (when polar is false)
      - toString: Should alternate on each different move between a slash character (/)
                  and a backslash character (\) starting with a slash.
      - getMove:  always infect if an enemy is in front
                  otherwise hop if possible
                  otherwise turn left.
