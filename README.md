# si507_project_04_hazita
Henny Tasker

I forked this project from https://github.com/si507-w19/Sample-Pyglet-Code
Original authors: Paul Resnick and Sam Carton

I made the follwoing modifications to the file basepong.py:

1) Made a single-player version
  a) changed the ball's initial angle
  b) deleted the Player 2 paddle
  c) changed the right-hand wall to a BallDeflector object instead of an EndLine object
2) Created a brick wall
  a) added a Brick class which acts as a BallDeflector object (inherits those attributes)
  b) remove each brick as the ball hits it
3) Keep track of hits (and every tenth hit, the game speeds up)
4) increased the frame rate
5) Keep score and include instructions for play (keys to press)


## An Overview of Basepong
Basepong is an arcade-style game similar to Atari's Breakout. Basepong was created by Sam Carton. The object of the game is to move the paddle to deflect the ball past your opponent's paddle. This version of basepong, however, is a single player game. In this version, the game is over when the computer scores a point.

##Pyglet in a Rush
Pyglet is a python library, most commonly used for developing games.

##The Game
First, a class GameObject is defined. This class uses some built-in features of the Pyglet library to create a 'sprite' or game object onscreen.
Sprites include the paddles, the ball, the endlines, and the bricks.

A game window is also defined, again by using inbuilt features of the Pyglet library.

##Game Objects and Action Classes
Different objects or sprites have different actions they can take. The first class of action is that of a BallDeflector. BallDeflectors deflect the ball. They do not otherwise interact with the ball.
Endline is another class of objects. While Endlines inherit properties from BallDeflector, they also result in the game being paused, and someone getting a point.
Paddles inherit from BallDeflector, too. However, Paddles are moveable.
Bricks inherit from BallDeflector, and are removed when they are touched by the Ball object.
