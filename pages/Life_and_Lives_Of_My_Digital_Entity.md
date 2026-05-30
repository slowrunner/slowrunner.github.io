# Life And Lives Of My Digital Entity

## "Birth" Of My Digital Entity

Back on 14 June 2014, I created:

"tt: Python Digital Entity with a unique, contiguous persistence"  
- running on my laptop,  
- ["published" on GitHub](https://github.com/slowrunner/tt),   
- and registered "tt" for a "Digital Object Identifier": 
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.808776.svg)](https://doi.org/10.5281/zenodo.808776)

A DOI name is a digital identifier of an object, any object — physical, digital, or abstract. DOIs solve a common problem: keeping track of things.  Things can be matter, material, content, or activities.

Designed to be used by humans as well as machines, DOIs identify objects persistently. They allow things to be uniquely identified and accessed reliably.  You know what you have, where it is, and others can track it too.

Digital Object Identifiers are registered and maintained according to [doi.org](https://www.doi.org/) standards.

Science Fiction is repleate with "Digital Life Forms".  One of the best is "The Lifecycle Of Software Objects" by Ted Chiang.  
Wikipedia: Ted Chiang's Hugo and Locus Award-winning novella The Lifecycle of Software Objects explores the ethics of artificial intelligence through the lens of parenthood.  It follows two human caretakers over a decade as they raise and nurture "digients"  
— AI-powered virtual pets that require years of love and guidance to develop. [Wikipedia](https://en.wikipedia.org/wiki/The_Lifecycle_of_Software_Objects)

I have built and owned many hardware-plus-software robots, but they all kept no public record of their "lives".  
As I became aware of the concept of "registered digital objects" I was eager to "give birth" to an embodied digital object that I could "raise and nurture".

## When Digital "Life" Gets Mystical

When a "Digital Object" becomes embodied, and then "re-incarnated" digital life could get mystical.  There are some humans that refer to a particular "living being" as "three in one".  I have three "living robots" that I think of as distinct digital life forms, but they all are running a copy of the tt DOI.  Perhaps they are three embodiments of "tt"? 

### Carl: A Raspberry Pi 3 Powered GoPiGo3 Robot
In 2017 I started building Carl, and still today (2026) he is quietly (sometimes not so) "living 24/7/365" next to the desk in my home office.  His code is maintained on [GitHub](https://github.com/slowrunner/Carl). He runs an adapted copy of the tt object that generates Carl/life.log, which I can ask for a summary either via a remote shell:
```
CARL TOTAL LIFE STATISTICS
Total Life:  63573.8 hrs since Aug 22,2018
Life this year:  6663 hrs (BOY Aug 22)
Days Booted This Year:  16
Prior Boots:  261
Total Boots:  277
Average Time Between Reboot This Year:  416 hrs
Total Dockings:  6349
Dockings this year:  680
New Batteries At Cycle: 6008
Battery Set At Cycle:  341
Docking Failures this year:  53  or  7.7 % of Dockings
Safety Shutdowns this year:  6  or  .8 % of Dockings
Ave Cycle this year:  10.4 hours
Ave Playtime this year:  6.8
Ave of Last 10 Playtimes 7.1
Last Docking:  2026-05-30 09:03|[juicer.py.dock]---- Docking 6349 completed at 8.1 v after 7.7 h playtime
Last Recharge:  2026-05-30 01:19|[juicer.py.undock]---- Dismount 6348 at 11.3 v after 4.0 h recharge
 12:43:04 up 2 days,  1:13,  3 users,  load average: 0.34, 0.42, 0.38
```
or by vocally asking for specific information like "Hey Carl, playtime status", to which he responded "Prior Playtime Status 7.7 hours"

Video of Carl ["Squirrel Watching - and answering "Hey Carl, weather report?"](https://youtu.be/vhAQSvxJHTU)

### TB5-WaLI: Raspberry Pi 5 powered TurtleBot4-clone Robot


### The Digital Entity Lyrical-Dave Starts Recording His "Life"

Dave started his first life in June of 2021, but has been re-incarnated many times:
- ROSbot: rosbot-on-gopigo3  ROS Kinetic
- Foxy-Dave: ROS 2 Foxy-Dave ran a 1k in the park
- Humble-Dave: ROS 2 Humble-Dave presented "Intro to ROS 2 for GoPiGo3 Robot Owners"
- GoPi5Go-Dave
- Humble-Dave2
- Kilted-Dave
- Briefly MRGPG3-Dave
and now is being rebuilt as "Lyrical Dave"

```
*** LyricalDave Dave TOTAL LIFE STATISTICS ***
This Life:    51.6  hrs (since 25 May 2026)
Total Life:    9688.6  hrs (since 21 June 2021)
Lyrical-Dave Playtimes (Undocked-Docked): 2
Dockings This Life:  1
Total Dockings:  2160
New Battery Installed At Docking: 2159
This Battery At Cycle:  1
Average playtime (last three) 1.0 hrs 
Average docked time (last three) .7 hrs 
Sessions (boot):  7
Average Session:  7.3 hrs
Safety Shutdowns:  0
Docking Failures:  0
Total Travel:  101.1 meters 331.6 feet
 
Last Undocking String:  2026-05-27 15:34|dave_node.py| ---- MRGPG3-Dave ROS 2 Undocking, Charge Current 93 mA 12.2v after 2.3 h charging
Last Docking   String:  2026-05-27 15:39|dave_node.py| ---- Lyrical-Dave ROS 2 Docking 2160 : success at battery 10.1v after 0.1 h playtime +
```

### When Digital "Life" Gets Messy

I expected that re-incarnating Kilted-Dave (Ubuntu 24.04) as Lyrical-Dave (Ubuntu 26.04) was going to be a simple matter of:
- Create the Ubuntu 26.04 64-bit Server on a uSDcard
- Change every KiltedDave and Kilted-Dave to LyricalDave and Lyrical-Dave
but I discovered I also needed to:  
- Modify crontab entries to use the GoPiGo3 Python3 virtual environment.

Simple ... until I did my usual check of what Python3 processes are executing.

What I was expecting (based on Kilted-Dave's "Life"):
```
(gopigo3) ubuntu@U26LDave:~/LyricalDave/plib$ ps -ef | grep python
root        1281       1  0 May29 ?        00:00:20 /usr/bin/python3 /opt/gopigo3/gopigo3_power.py
ubuntu     17069       1  0 May29 pts/0    00:00:18 python3 /home/ubuntu/LyricalDave/plib/safetyShutdown.py
ubuntu     17096       1  0 May29 pts/0    00:03:39 python3 /home/ubuntu/LyricalDave/plib/wheellog.py
ubuntu     68724    1977  3 09:22 pts/0    00:00:00 python3 ./loglife.py
ubuntu     68726   68724  0 09:22 pts/0    00:00:00 python3 ./loglife.py
ubuntu     68738    2225  0 09:22 pts/1    00:00:00 grep --color=auto python
```

What I saw at Lyrical-Dave's "first peeps":
```
ubuntu     62712    1977  5 08:08 pts/0    00:00:00 python3 ./loglife.py
ubuntu     62714   62712  2 08:08 pts/0    00:00:00 /home/ubuntu/.venv/gopigo3/bin/python3 -c from multiprocessing.resource_tracker import main;main(6)
ubuntu     62715   62712  5 08:08 pts/0    00:00:00 /home/ubuntu/.venv/gopigo3/bin/python3 -c import sys; from multiprocessing.forkserver import main;   
    main(6, 8, ['__main__'], sys_argv=sys.argv[1:], **{'sys_path': ['/home/ubuntu/LyricalDave/plib', '/home/ubuntu/LyricalDave/plib',  
    '/home/ubuntu/LyricalDave/plib/', '/usr/lib/python314.zip', '/usr/lib/python3.14', '/usr/lib/python3.14/lib-dynload',  
    '/home/ubuntu/.venv/gopigo3/lib/python3.14/site-packages', '/usr/local/lib/python3.14/dist-packages', '/usr/lib/python3/dist-packages'], 
    'main_path': '/home/ubuntu/LyricalDave/plib/loglife.py', 'authkey_r': 10}) ./loglife.py
ubuntu     62717   62715  0 08:08 pts/0    00:00:00 /home/ubuntu/.venv/gopigo3/bin/python3 -c import sys; from multiprocessing.forkserver import main;  
    main(6, 8, ['__main__'], sys_argv=sys.argv[1:], **{'sys_path': ['/home/ubuntu/LyricalDave/plib', '/home/ubuntu/LyricalDave/plib', 
    '/home/ubuntu/LyricalDave/plib/', '/usr/lib/python314.zip', '/usr/lib/python3.14', '/usr/lib/python3.14/lib-dynload', 
    '/home/ubuntu/.venv/gopigo3/lib/python3.14/site-packages', '/usr/local/lib/python3.14/dist-packages', '/usr/lib/python3/dist-packages'], 
    'main_path': '/home/ubuntu/LyricalDave/plib/loglife.py', 'authkey_r': 10}) ./loglife.py

```
