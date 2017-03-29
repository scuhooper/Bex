# Prominent Features
## Character Actions
One of the highlights of the project is the amount of things the player is able to do. Although there are a number of options, the character cannot break animations to begin things early.

- ### Jumping
To handle the character being able to jump, a small, thin trigger collider was placed on the bottom of the character's sprite. Anytime the trigger has a trigger enter event, it sets the boolean for being on the ground to true for the player. When there is a trigger exit event, it sets the grounded boolean to false preventing the character from jumping.

- ### Dashing
Like the _Mega Man Zero_ series of games, the main character, Bex, can dash giving her a short burst of speed over a small distance that prevents her from jumping, attacking, or changing direction. The dash is only performable if the player is on the ground and the speed doesn't transfer to a jump. This allows the player to make a quick escape from enemies or projectiles, but forces them to choose the speed boost over fine control of the character.

- ### Attacking
In the game, the player has a ranged attack of shooting their plasma gun or can perform a melee attack which kicks to whichever direction the player is facing. The attacks can take place while running, stationary on the ground, or jumping. Executing a kick in the air starts a quick descent at an angle where the player attempts to kick anything in its path to the ground, and the kick on the ground makes the player stop while it transpires. While the jump kick can't change direction, the player can change direction while jumping and shooting.

<br />
<hr>

## C# Interface Classes
This project involved several classes that share several similar functionalities, but each would need their own implementation. I consider using inheritance with virtual functions, but I wanted to make sure these functions were declared and had their own definitions. I decided to make C# interfaces to handle these requirements. This allowed me to make a class inherit from an interface which requires the interface be implemented for the code to compile. By making the files have descriptive adjective names, it flows logically when anyone else would go to implement or inspect the code.

<br />
<hr>

## Scrolling Menu Screen
The title screen for _Bex_ is actually done as a few simple methods hacked together. The sprites for the forklift and Bex, the main character, are just animations on a constant loop. The background is being moved each frame with a math function that allows for a number to be always be between zero and a specified value using the modulo operator. As the scene moves, a coroutine causing the screen to gradually fade to black. After the scene resets to the beginning point, the black overlay is made clear again.

<br />
<hr>

# Code Repository
## [Bex Repo](https://github.com/scuhooper/Bex)
