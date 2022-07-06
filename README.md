<p align="center">
<img width="20%" src="assets/images/icon.ico" alt="Floppy Sticks Logo">
<br/>
<br/>
< <a href="#2-installation">Installation</a> |
<a href="#3-features">Features</a> |
<a href="#5-requirements">Requirements</a> >
<br/>
< <a href="#4-how-to-play">How to Play</a> |
<a href="#6-extra">Extra</a> >
</p>

# **Floppy Sticks**

## 1. Description

Floppy Sticks is a 2D puzzler inspired by a numerical method used to integrate Newton's equations of motion.  
Despite the ***silly*** name....  
Floppy Sticks emits a rather relaxing and statisfying atmosphere when playing.

## 2. Installation

*     git clone https://github.com/Parallaxi/Floppy-Sticks.git
* [**Itch.io** (*Coming Soon*)](https://parallaxi.itch.io/)

## 3. Features

* Start Menu :arrow_forward:
* Tutorial :dart:
* Visual Effects :sparkles:
* Dynamic Background :cyclone:
* Notifications :bell:
* Music & Sound :musical_note:

## 4. How to play

The goal of the game is to convert all the given points into dynamic points.
There exist 3 types of points (*clickable*, *dynamic*, *static*) in the game, which are represented by differently coloured circles.

1. <img src="assets/images/points/clickable.png" alt="Clickable"> ***Clickable***
   * Initially they are static and don't move. However when clicked they turn into dynamic circles.
2. <img src="assets/images/points/dynamic.png" alt="Dynamic"> ***Dynamic***
   * On conversion, they become affected by gravity and will begin to fall.
3. <img src="assets/images/points/static.png" alt="Static"> ***Static***
   * Spends most its life locked in place, the only way to convert it into a dynamic circle is to knock it with a dynamic circle.

## 5. Requirements

* Python >= 3.10
* Pygame >= 2.0

## 6. Extra

If you come from a Game Developement background, you've probably heard of [**Euler Integration**](https://en.wikipedia.org/wiki/Euler_method). This is a numerical method that is used very often for movement in games. This method is by far the simplest and easiest to implement. However up to a point this method becomes very inaccurate when using larger more precise numbers.
This is why Floppy Sticks makes use of [**Verlet Integration**](https://en.wikipedia.org/wiki/Verlet_integration "Wikipedia"). Verlet allows for more accurate and realistic movement.

Here is an example of how you implement both integrations.

```python
# Euler Integration
position = position + velocity
```
```python
# Verlet Integration
velocity = position - last_position
last_position = position
position = position + velocity
```

This creates surprisingly realistic behaviour.

# 7. Credits

* MUSIC CREATOR - [Context Sensitive](https://www.youtube.com/c/ContextSensitive)
* ORIGINAL IDEA - [Supernapie](https://supernapie.com)

# 8. License

**Floppy Sticks** is licenced under an MIT licence.
