# HOW TO RECOVER AN ACCIDENTALLY MERGE

NORMAL STEPS:
+++++++++++++
- create b1
- cm1 > b1
- Push b1
- create b2
- cm2 > b2
- push b2
- checkout b1
- cm3 > b1
- Push b1
----

MISTAKE STEPS (ACCIDENTALLY MERGE):
++++++++++++++
- checkout b2
- Pull b1
- (b2's log: 
	cm merge
	cm3
	cm2
	cm1
)
- Push b2
=====

RECOVERY STEPS:
+++++++++++++++
- checkout b2
- checkout c2
- (b2's log:
	c2
)
- git push -f origin HEAD:b2
- git reset --hard origin/b2
