# 5M-godz-newped-wpolyzone

FiveM Script to spawn new ped with QB-Target and Polyzone selection of Triggering Events
<BR>
<BR>
This one fixes the issue that if other ped spawns as npc randomly in world it will show the QB-Target to trigger events. But since its triggered to a polyzone it fixes that issue.
<BR>
<BR>
Change Ped Spawn location in config.lua called ```Config.Peds```

```lua
Config.Peds = {
    -- { x, y, z, ped heading, model hash, ped model, heading text, animation info }
    {267.45, -624.04, 44.0, 65.94, 0x9D0087A8,"ig_claypain", "Gangster", "amb@world_human_aa_smoke@male@idle_a"}
}
```
https://wiki.rage.mp/index.php?title=Peds to get Model Hash, Ped Model
<BR>
<BR> 
```lua
  exports['qb-target']:AddBoxZone("NewBoxZone", vector3(309.8, -602.05, 43.29), 1, 1, {
        name = "NewBoxZone",
        heading = 70,
        debugPoly = Config.DebugPoly,
        minZ=40.09,
        maxZ=44.09
```
<BR> To get this info you will need to know how to use Polyzone. Good video to watch is from here https://www.youtube.com/watch?v=O6KWDGARciU
<BR>
Change Icon in client.lua look for ```icon = "fas fa-fist-raised",```
<BR>Example: ```icon = "fas fa-plus-square",```
<BR>Using from https://www.w3schools.com/icons/default.asp
<BR>
<BR>
Change Event in client.lua look for ```event = "TRIGGER-EVENT",``` 
<BR>Example: ```event = "hospital:client:dothis"```
<BR>
<BR>
Change Label in client.lua look for ```label = "Raise Your Fist!",``` 
<BR>Example: ```label = "Check In",``` 
