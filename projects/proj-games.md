---
layout: post
title: 'Games'
---

I've been creating games with Processing, GameMaker, Godot and Unity (even ROM hacking) for many years now, here's some of my recents experiments !

---

#### Project Karoiju

{% include youtubePlayer.html id="SPCbvTvk6vA" %}

With this project I wanted to learn the whole process between creating a character mesh, animation and textures to its Unity implementation.
I've written my own character controller logic, based on raycasts.

I've modeled, rigged and animated this character with Blender and did the texture with Photoshop.

{% include youtubePlayer.html id="ANQvbX9fFxI" %}
*The character animations are pretty rough, it was my first experience animating in 3D. But I've learn a lot !*

{% include youtubePlayer.html id="ZS1qpMIHCPw" height="700" %}
*It was my first time texture painting in Blender aswell !*

---

#### Super Pépin Bros.

A NES ROM hack in the universe of [Kékéflipnote](https://twitter.com/Kekeflipnote).

{% include youtubePlayer.html id="_ia_PPuo4Is" height="613" %}
*A playthrough of the first world.*

A fun project where I had to play with the limited resources of the cartridge and the console !
Pixel art with limited palette is pretty challenging.
I had to write a little bit of assembly code to modify the game, like disabling the palette flipping of the fire flower (a handled console sprite in my hack !) power up, keeping the same color.

---

#### Rocket Man

A Unity game done during ENIB's game jam created around the rocket jumping mechanics !

{% include youtubePlayer.html id="MsORDpliISY" %}

A fun little problem encoutered : firing a rocket from the weapon and still be able to aim towards a target in the middle of the camera view :

{% include image.html image="projects/proj-games/raycast.png" %}
- 1 : Firing from the camera, the trajectory works well, hiting the target, but the missile doesn't starts from the weapon end.
- 2 : Firing from the weapon is the opposite, trajectory is wrong, but the missile starts from the weapon end.
- 3 : Best of both world : First, raycasting from the camera, getting the target position of the missile, then instianting the missile from the weapon end towards the target.

---

#### Tako's Project

A 2D Unity game to experiment with the Universal Render Pipeline, lights it provides and pixel perfect rendering with Cinemachine.

{% include youtubePlayer.html id="YJPhRjLT6JI" %}
