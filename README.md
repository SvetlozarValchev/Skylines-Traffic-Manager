# Skylines-Traffic-Manager 1.04rc

This mod lets you add priority roads, control traffic lights, change lanes and add/remove crosswalks. 

# Features: 

# Add/Remove Traffic lights 
- You can add/remove traffic lights on all road junctions 

# Priority Signs 
- Set main and secondary roads. 
- Diamond(yellow) sign is main road, all cars on that road have a priority over all other roads. 
- Triangle(red and white) sign is secondary road, cars have to yield to vehicles from the main road. Stopping is not required. 
- Stop sign is also a secondary road. Cars have to stop, look for incoming cars and if the road is clear - continue on their trip 

# Manual traffic lights 
- Manually control all traffic lights on a junction 
- Useful for designing your timed traffic lights (See 'Timed traffic lights'), clearing traffic and role-playing as a traffic cop 
- Important: Traffic lights revert to normal when inactive 

# Timed traffic lights 
- Set traffic light timers on one or more junction to allow for more heavy routes to clear more traffic. 
- Configure multiple junctions at once to create a green wave. 

- For people asking how to use it, here's a simple how-to: 

1. Select timed traffic lights. 
2. Select the desired junction (select one 4-way junction for a first-timer) 
3. Click next. 
4. Click Add State 
5. Set the desired lights on the junction (don't click 'mode', as you want to use the simplest light for a first-timer); Example: set the 2 roads facing each other - green; and the other 2 - red 
6. Set the desired amount of seconds you want the lights to be with the slider (for example: 12) 
7. Click 'Add' 
9. Click 'Add state' 
9. Set the desired lights on the junction (again, don't click 'mode' - you want simple traffic lights); Example: reverse the lights - the ones that are red - make them green, and the ones that are green - make them red. 
10. Set the desired amount of seconds you want the lights to be with the slider (for example: 8) 
11. Click 'Add' 
12. Click 'Start' 
13. Now you have a junction that has a 4-way with one of the roads having 12 'seconds' of green time (it's not exactly seconds, but it's an easier naming) and the other having 8 'seconds' of green time 

This will give you a basic idea of how things work. You can watch the video for more complex timed traffic lights. 

# Change lanes - see 'compatibility mode' below if you do not have this option 
- Change road lanes to allow/disallow lefts/rights, add more forward lanes, etc., traffic will start following it after 2-3 minutes. If you want cars to instantly start following them, use 'Clear traffic' button (See 'Clear traffic') 
- Important: these lanes define the direction, not the road curve, so if you have a T-intersection with 45 degrees curve, forward is forward, not left/right. Sometimes you'll have to do it manually, since the base game does NOT do it that way) 

# Clear traffic 
- Clears all road traffic 
- Useful when changing lanes, creating manual/timed traffic lights and to clear congestions caused by bad road planning. 

# No despawn - see 'compatibility mode' below if you do not have this option 
- Enable/Disable despawning caused by traffic congestion or traffic being blocked. 

# Same road priority (base - not configurable) 
- All cars that are on a same priority level (diamond - diamond, yield - stop - yield - stop), manual traffic lights, timed traffic lights or on modified lanes start to follow the rules for Priority on the right and wait for left turn(wait for right turn in LHD) 

# IMPORTANT 
All roads that have priority signs, enabled manual traffic lights, timed traffic lights or changed lanes automatically start running under an additional layer - Traffic Manager's simulation. Everything else runs under game's simulation 
Which means that cars start following the assigned lanes and same road priority. The base game sometimes assigns lanes that are not correct, which will cause traffic to not go through that intersection. You'll have to manually fix the lanes to the proper ones, so the traffic can start functioning again 

# Known issues: 
- No 'save to cloud' support 

# Incompatible mods (please report which ones it does not work correctly with): 
- Zonable pedestrian roads 
- Lane changer 
- Toggle traffic lights 
- All mods that override the Pathfinder; CarAI.CalculateSegmentPosition (both methods); CarAI.SimulationStep; RoadBaseAI.SimulationStep; HumanAI.CheckTrafficLights; PassengerCarAI.SimulationStep, CargoTruckAI.SimulationStep; 
- All mods that modify NetNode and NetLane flags. 
(Yes, I know it sucks, I also want a common API/NAM/CKAN, but that will take some time) 

# Compatibility mode: 

When it encounters that another mod is overriding the PathManager, it disables 'Despawn' and 'Lane Changer' tools so it doesn't cause problems. 
Tested only with Traffic++ 

Please check yourself if your issue is caused by another mod, it's pretty hard to go through every mod and check if every functionality is working properly 

It's important to check if your issue is caused by another mod. Disable and restart the game just to be sure. Some mods do not break everything in the mod, just parts of it, and debugging becomes very difficult. 

How to clear ALL traffic manager saves in case a major/blocker bug pops up: 
Open your Steam folder, go to SteamApps\common\Cities_Skylines\Cities_Data, delete all files with the name 'trafficManagerSave_xxxxxxx.xml' 
