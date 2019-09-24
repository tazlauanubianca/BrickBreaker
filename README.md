# Brick Breaker Game

The purpose of the project is to create a 2D game in which the user controls a platform. The platform guides a ball that hits the bricks.

The scene contains the following objects:

* platform (a filled rectangle)
* walls: left, right and top wall (filled rectangles)
* boll (a circle disk)
* at least 5 x 10 bricks (filled rectangles)
* number of lives of the player (for example, each life can be represented by a circle disk, similar to the ball)
* powerups

## Gameplay

The purpose of the game is to destroy all the bricks in the scene.

The platform is controlled by the player by moving the mouse. At the mouse click, the ball is sent to the scene. The ball moves continuously in the direction given by the platform or by reflection, at the collision with the walls and bricks. If the ball reaches the bottom of the stage and is not saved by the platform, the player loses a blanket (and the number of objects on the screen representing lives is reduced).

When the ball is launched on the stage, it is sent along the vertical direction. At the collision with the platform, the direction is changed. If the ball hits the platform in the middle, the direction of reflection will be vertical. If the ball hits the platform on the left, then the direction of reflection for the ball will be to the left of the platform. Analog on the right side. The figure below explains the reflection on the ball platform. You can imagine that the platform represents the axis of the cosine on the trigonometric circle and the position where the ball hits the platform, even the value of the cosine. If the ball falls on the middle of the platform, then cosinus = 0. If the ball falls on the right side of the platform, cosinus is between 1 and 0. If the ball falls on the left side of the platform, cosinus is between 0 and -1. The ball is reflected from an angle equal to the arccosinus.

When colliding with the other elements in the scene (walls, bricks), the ball is naturally reflected (for example, in a collision with a vertical wall, if x and y increased until the moment of collision with steps tx, respectively ty, after collision y increases further with the ty step, but x starts to decrease with the tx step).

When the ball collides, the bricks disappear gradually (they are scaled down for 1-2 seconds).

The game was implemented in 3 Vis 2D Lab and can be run from
the main file. The main file is now configured to run the game.

To move the platform left-right, you must move the mouse. Blackboard
game has bricks in 3 different colors having the following meanings:
1. Normal bricks that will break at the first shot of the ball
2. Bricks that once hit will play a power up
3. Bricks that require two hits to be destroyed

The powerups available in the game are of two types and are signaled by
two types of hunting objects:
1. A powerup that makes the ball move much faster
2. A powerup that brings the ball back to the platform to be launched
again in execution

The game has 4 lives: the starting one and 3 auxiliary lives. A life is lost if
the ball comes out of the play space, that is if it falls and is not caught by the platform
