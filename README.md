To make a mod for any gamemaker studio game, you will need [undertalemodtool. 
](https://github.com/UnderminersTeam/UndertaleModTool)
These files will help with the framework around the achievements (mainly communicating with the Retroachievements website).

Unfortunately, it's not effortless to implement this, so here's a guide. If it's unclear, or you need help with standalone modding, feel free to ask me for advice.

First, you should go to the room list and locate one of the rooms at the start (such as a splash screen, for example.)

There will be in one of the objects in it's code a room_goto_next() or a room_goto(roomnamehere). You should create a room called "RA_connect".

Then, replace the room_goto with room_goto(RA_connect). 


Add a script called RA_achievement_trigger and copy and paste the code given. 


Create the objects RA_achievement_hud (set this one as persistent) and RA_MENU. 
Put RA_Achievement_Hud in the starter screen and RA_MENU in the RA_connect room. 

For each object, add the code in the folders to the matching category.

Fill in the information in RA_MENU_CREATE.

Congrats! You're done! Now just the "easy" part of coding all the achievements. To make the user unlock an achievement, use the achievement trigger example.
