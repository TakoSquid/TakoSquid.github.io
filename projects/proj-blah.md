---
layout: post
title: 'Blah Thingy'
---
Blah Thingy is a collection of libraries and tools built on [blah](https://github.com/NoelFB/blah) to help create 2D games in C++.

You can acces the repo [here !](https://github.com/TakoSquid/blah-thingy)

---

#### Quick demo : Debugging tool

{% include youtubePlayer.html id="QtSivZ5ahtI" width=700 height=535 %}

---

#### Features

##### A World / Entity / Component system :

{% highlight cpp%}
auto en = world->add_entity(point);
en->name = "player";

auto anim = en->add(Animator("player"));
anim->play("idle");
{% endhighlight %}
Here, we simply add an Entity to a World and then adding a animator Component to it.
Note that we can acces Entity's and Component's public fields and functions.

##### Few of the already existing Components...
- Animator : acces and play animations from an [Aseprite](https://www.aseprite.org/) file.
- Collider : add collision and collision mask to an Entity. Currently basic shapes and slopes are available.
- Signal_Box : observer pattern implementation. Add a reaction upon signal reception from other signal boxes.
- And more !

Each Component can provide a debugging display, used when the debug GUI is enabled.

##### ... but you can freely create new Components !
You only have to create a derivated class from Component.

{% highlight cpp%}
class Talkative : public Component
{
public:
    void awake() override;
};

void Talkative::awake() {
	Log::info("I'm awake !");
}
{% endhighlight %}
*A simple Component outputing a message when Entity is awake.*

##### Ogmo map parsing
Maps can be created with [Ogmo](https://ogmo-editor-3.github.io/).

You can create map with collisions and slopes. Map name will be its position in the world.
Entity position can also be set as so as Signal Boxes links through JSON files.

{% include image.html image="projects/proj-blah/ogmo.jpg" %}
*Ogmo map editor : Multiple layers, blocks and entities (the wide red rectangle is a moving platform with its path)*

##### Debugging tool
You can select an object from the list or in the game window and tinker with its Components values ! 
Created with [Dear ImGui](https://github.com/ocornut/imgui).

{% include image.html image="projects/proj-blah/blah_ui.jpg" %}
*Every Components overriding the debug method can display info in the game window and/or in the right column.*

