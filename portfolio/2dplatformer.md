---
layout: default
---


A partially complete 2d platformer made in Godot.  It was a solo project made as part of an online course in game design offered by MSU.

<img  src="images/platformer2d.png"/>

It was ultimately abandoned along with the rest of the course after becoming disillusioned with the online course's lack of feedback and engagement. The code and assets provided by the course were for a Unity project, but I rebuilt them in Godot as an exercise. I was still in the middle of working out mechanics, movement, and camera behavior, so there is only one level and some simple obstacles made for testing.  

#### Development
The biggest problem I was working on is the lack of engaging core mechanics to design gameplay around.  There are some assets like enemies, moving platforms, and health pickups that were made but not yet used or tested in any actual gameplay.  But fundamentally, the game needs more elements that interact with the player and give them meaningful agency.  Ideally, new elements should add new challenges involving timing, sequencing, and exploration.  New tiles like crumbling platforms, new interactables like switches, and new reactive enemy behavior are some examples of such elements that could be used in all of these ways.  Adding new player movements such as: wall kicks, a dash, climbing and ledge grabbing could also help.  Provided it were accompanied by connected elements designed around them.  

I was also still debating how to structure the game experience overall. It currently just has a simple course clear structure, but there were a few directions I was considering focusing on. 

One aspect I had planned to eventually focus on was environmental storytelling and obstacles to give the game a simple narrative.  Personally, I find having a narrative in mind helps me come up with gameplay elements, and for this project I had a narrative around a "space engineer."  They need to stop the moonbase facility's AI gone rogue and its army of robots to save the day.  It's not the most original or nuanced narrative, but it's plenty to help get some ideas for a simple game.

One idea was to give the player a "magneto-wrench" that they would use as their primary tool for interacting with the world. They would use it as a sort of grapple hook for movement, a weapon to throw and whack enemies with, and as a way to interact with level elements like switches and vents. 

<figure style="margin: 20px;" >
<img src="images/plat2d-unfinished.png"/>
<figcaption style="font-size:11px; text-align:center;">Basic enemies, health pickups, and moving platforms were implemented, but had yet to actually be used in a level.</figcaption>
</figure>


#### Strengths & Weaknesses
One area that I'm mostly satisfied with is the camera movement.  The code originally provided just locked on to the player, keeping them at the center of the screen at all times.  The problem with this simple approach is that it effectively makes the level constantly moving as you navigate it, removing some sense of visible progress through the level and making tricky platforming feel bad. Particularly the up and down movement of just jumping becomes sort of nauseating.  So for even basic movement to work well, the camera behavior needed reworking. 

With some trial-and-error, I made two key changes. First, I added a deadzone to the camera and an interpolated delay, making the player drag the screen with them.  I'm not entirely happy with this solution as it makes the space in front of the player less visible, but it does at least help with the camera movement while jumping. Second, I added hard camera boundaries.  Critically, this allows for the ground to be at the bottom of the screen, giving the player room to jump without the camera bobbing.

However, a key feature that is still missing from the camera is the ability to add soft camera boundaries to break up the gameplay into rooms.  This would allow for much less camera movement and an overall better experience.  It would also provide a natural delineation to the gameplay using the camera, with each room effectively being a single challenge or mini-level containing a few puzzles or gameplay moments.  Ideally, this would both give it a more clear structure to the player, and make designing it easier.  The bite-sized nature of it would also be an advantage in the context of a vertical slice, as you can add, reorder, and remove rooms easily without worrying about completely breaking the overall game structure.

As a crucial element to the feel of a platformer, I was focused on getting it fixed first, so there are plenty of other small touches like input buffering that are still missing.

#### Lessons learned
The core take away from this project for me though, was the need for other people.  Without anyone to share ideas with or get advice and feedback from, everything is harder, slower, and not as good as it could be.  You don't get the chance to see anything outside of your own perspective and assumptions.  Equally as important, the motivation and purpose that community gives is missing.  Games are made for people to enjoy.  If they're only made for the developer themselves, then it's all too easy for them to completely lose purpose and be left unfinished.


Test build:&emsp;*<a href=""><s>github.com/mvestrand/msu-2dplatformer</s></a>* <br>
Source code:&emsp;*<a href="https://github.com/mvestrand/msu-2dplatformer">github.com/mvestrand/msu-2dplatformer</a>* <br>


<hr style="clear: both">
