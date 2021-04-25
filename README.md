# FlappyBird

Flappy Bird is a side-scrolling mobile game featuring 2D retro style graphics. The
objective is to direct a flying bird which moves continuously to the right, between
sets of pipes.

**Constraints :**
1. If the player touches the pipe, they lose.
2. The bird briefly flaps upward each time that the player taps the screen; if the
screen is not tapped, bird falls of because of gravity.
3. Each pair of pipes that the bird navigates between earns the player a single
point.
4. If the bird exceeds the screen margins, the game overs.

Technology Stack used :
1. Java SE 1.8 JDK toolkit
2. Android Studio Gradle Build 3.4.1
3. OpenGL Based GDX1.6 Library by Third Party Vendor Badlogic Games
4. Vector assets by Badlogic games
5. Android SDK API 22.0.1


**Approach Used:

The Flappy Bird game makes the use of stunning vector assets which are
redesigned as per the guidelines of Nintendo Games and makes the usage of GDX1.6
library to perform the triggering and manipulation of events.
The game starts where the bird is visible with a background on the screen.
Factors such as velocity, gravity, speed of pipes .etc is taken care by the programmer
and can change its values as per his/her need. And these factors can also help in
determining the difficulty level of this game.

**1. Movement of bird :**

The movement of bird, its dynamicity is taken care of by the variables which
define the speed, direction and velocity of the bird. The X1,Y1 co-ordinate of
bird is maintained as per its motion and is carried forward throughout the
application. The X, Y value proves useful whilst determining the score of the
player.

**2. Movement of pipes :**

Movement of pipes is also managed similarly as the way its managed for the
birds. Moreover, an array of pipes is maintained which gets called repeatedly
throughout the game. This ensures reusability principle and makes sure that less
resources are called during runtime.
3. When the X, Y co-ordinate of bird exceeds that of any pipe, a point is awarded
to the player.
**4. Collision Detection :**
Though we’ve used images wrapped in a texture class, but we cannot predict
the collision of textures itself. For this, a ShapeRender class instance is maintained
which helps in maintaining the shape for the components that are used, like circle for
bird, rectangle for pipes. etc. This shape class uses an Intersector class’ method
named as overlaps() which returns boolean if collision occurred, else False.
All these concepts work in unison to make the game work efficiently.
