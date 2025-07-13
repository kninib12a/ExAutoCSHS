# ExAutoCSHS
An Addon for TurtleWoW for automatically alternating Crusader/Holy strike to maintain maximum uptime on the Zeal / Holy Might buffs 
This relies on CombatLog entries and internal timers, so even if you break rotation it'll manage to keep up with buffs

Usage : Create a macro with:
/AutoCS [openCS/openHS/openAuto] [moreCS/moreHS/moreAuto] [prioZeal] [exorcism]

- openCS opens with Crusader Strike,
- openHS opens with Holy Strike,
- openAuto opens with CS if using a 2h weapon, HS is 1h [default setting],

- moreCS will do 2 crusader strikes to ever holy strike,
- moreHS will only do CS when Zeal needs a refresh  so close to 3 HS per CS (for maximum threat tanking),
- moreAuto will do moreCS  with a 2h weapon , moreHS  with one handed weapon  [default setting],

- prioZeal will priorize getting zeal to 3 stacks regardless of rest of settings then proceed following them [disabled by default],

- exorcism will attempt to cast Exorcism if CS/HS is on CD and the target is valid [disabled by default]


Example: 

/AutoCS openHS prioZeal 

will open with HS, priorize building zeal until 3 stacks , then proceeds only doing CS when Zeal needs a refresh 
this results most of the time in :
HS-CS-CS-HS-CS-HS-HS-HS-CS-HS-HS-HS-CS-HS-HS-HS... 
----1-2-----3--starts doing 3 HS to CS 

/AutoCS openHS prioZeal exorcism
will do the same interwoven with exorcism : 
HS-Exorcism-CS-CS-HS-Exorcism-CS-HS-HS-Exorcism-HS-CS-HS-Exorcism-HS-HS-CS-Exorcism ...
