## Will & Fatigue Tweaks

The intent is to make Will a more compelling stat to have on a soldier and 
encourage players to synergize with existing game systems which were previously
undervalued due to the lack of penalties around having low will.


## Stat changes

1. Base will of new recruits: 20-45 (avg: 33)
2. Promotion Progression

Each class is split into a group that follows a specific progression: Low, Medium, High, and Highest.

Low Will classes: Sharpshooter, Specialist

Medium Will classes: Ranger, Shinobi, Gunner

High Will classes: Assault, Grenadier, Technical, Reaper

Highest Will classes: Psi Operative, Templar, Skirmisher


|          | Low Will | Medium | High  | Highest |
| ---      | ---      | ---    | ---   | ---     |
| Squaddie | 3        | 5      | 5     | 5       |
| LCPL     | 3        | 4      | 5     | 5       |
| CPL      | 2        | 2      | 3     | 4       |
| SGT      | 2        | 2      | 2     | 3       |
| SSGT     | 1        | 2      | 2     | 2       |
| TSGT     | 1        | 2      | 2     | 2       |
| GSGT     | 1        | 1      | 2     | 2       |
| MSGT     | 1        | 1      | 1     | 2       |
| Total    | 14       | 19     | 22    | 25      |
| Range    | 34-59    | 39-64  | 42-67 | 45-70   |
| Average  | 47       | 52     | 56    | 58      |


## Tired & Shaken changes

1. Tired occurs at 50% Will, takes 7-10 days to recover (reduced) 
2. Shake noccurs at 10% Will, takes 14-20 days (reduced)
3. Normal recovery takes 0 - 7 days

## WillEvent changes 

1. Lose 1 Will per turn. 

This is what soldiers will return as assuming a flawless mission. Please note 
that most Guerilla ops missions take about 10 turns. Most longer missions
like large maps, Facility, or Chosen stronghold assaults take about 20 turns tops. 
The final mission takes 20-30 turns.

| Will      | 10 Turns      | 20 Turns      | 30 Turns     |
| ---       | ---           | ---           | ---          |
| 20        | Tired         | Shaken        | Shaken       |
| 30        | Ready         | Tired         | Shaken       |
| 40        | Ready         | Tired         | Shaken       |
| 50        | Ready         | Ready         | Tired        |
| 60        | Ready         | Ready         | Tired        |
| 70        | Ready         | Ready         | Ready        |


2. Adverse WillEvents

This is a table of all the events which can harm Will in a mission and any associated panic information about them. 
All of these events occur when the unit is at the "Ready" state, so they happen to everyone. All events can zero out a
unit's Will. I believe all of these events (Except bondmate?) need to occur with line of sight to trigger the event for a unit.

| Event             | Chance to occur       | Will Lost                             | Panic Chance          | Panic Types        |
| ---               | ---                   | ---                                   | ---                   | ---                |
| wounded           | (100 - current will)% | HP % lost, so 50% = 5; 2 min, 10 max  | (50 - current will)%  | Panic, Shattered   |
| wounded teammate  | 100%                  | 2                                     | no                    |                    |
| wounded bond      | 100%                  | 3                                     | no                    |                    |
| dead teammate     | 100%                  | 5                                     | no                    |                    |
| dead bondmate     | 100%                  | 10                                    | (100 - current will)% | Berserk            |
| captured teammate | 100%                  | 3                                     | no                    |                    |
| captured bondmate | 100%                  | 5                                     | (100 - current will)% | Berserk            |
| teammate panic    | (100 - current will)% | 2                                     | no                    |                    |
| bondmate panic    | (100 - current will)% | 2                                     | no                    |                    |
| teammate mind-ctl | 100%                  | 2                                     | no                    |                    |
| bondmate mind-ctl | 100%                  | 3                                     | no                    |                    |
| teammate unconsc  | 100%                  | 2                                     | no                    |                    |              
| bondmate unconsc  | 100%                  | 3                                     | no                    |                    |
| horror            | (100 - current will)% | 5                                     | (100 - current will)% | Panic, Shattered   |


Here's a table which breaks down the `wounded` event based on a unit's current Will. Keep in mind, that the current Will means it's
the Will a unit has 'right now' in the mission, so starting Will MINUS the deductions from turns, adverse events, etc. 
This can turn into 0 on long, brutal missions for many units.

| Will          | Chance to lose Will      | Chance to panic if fires   |
| ---           | ---                      | ---                        |
| 0             | 100%                     | 50%                        |
| 10            | 90%                      | 40%                        |
| 20            | 80%                      | 30%                        |
| 30            | 70%                      | 20%                        |
| 40            | 60%                      | 10%                        |
| 50            | 50%                      | 0%                         |
| 60            | 40%                      | 0%                         |
| 70            | 30%                      | 0%                         |
