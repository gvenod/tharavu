# tharavu
tharavu - meaning data; --- record human pose in time series; replay to attain some specific skill.

# Goal:
 
Take an AI Idea to Production, Develop mobile app using pose net model to showcase edge ai development skills.

# Vision:

AI for skill development.

# Idea:

record human pose in time series; replay to attain some specific skill. 
skill can be yoga, dance move, karate, hardware assembly, moving things......

using pose net ai model running on edge, in 'record' mode collect relative position of human body joints, in 'replay' mode assist/watch for relative position of joints and help user to attain the pose. 

for example: in headstand yoga pose; joints head/hand elbow on the bottom, hip in the middle and toes on the top. both legs together and body in straight line.
user 1 [yoga instructor] records above scenario as pose data and share it with user 2 [student].
user 2 [student] in replay mode, try to do the same pose, app will capture and give feedback on student pose. [say instructs user if body pose is wrong, if app found toe joints are on the floor, app will ask user to raise the leg....]


# Customer use case:

* use case 1. fun - friends can share time bound pose challenge 
* use case 2: yoga/karate/taekwondo instructor - pose correction; instructor will record the pose, share with students to practice. app will capture the practice session and correct the student posture; share data with instructor back.
* use case 3: offline dance collaboration - set of dancers can practice individually; instructor can record and share sequence of dance steps; so co dancers can practice offline. app will correct dance steps and assist with learning/honing the skills.
* use case 4: gym 
* use case 5: hardware assembly steps.


# reusability
 1. pose net currently outputs position of human joints x,y,z location in a given picture. 
conversion of this data to relative position of human joints make it portable to be applied on any human [different height, shape and size] and any image; 
conversion algorithm has to be a reusable library


# Application Goals:

1. ai inference on android
	1. use android litert runtime
	2. use kaggle posenet model
2. refresh android knowledge
3. framework for reusability/enabling new use cases
4. simple: record and replay; no ndk only kotlin java
5. open source  & updateable
6. Expandable/customized easily 


# revenue model:

1. free; open source under GPL v3


# app features:

 camera capture
 ai models
 database
 settings store and retrieve
 share
 activity/fragment
 file access/create/load/parse
 share data
 text to speech
 overlay of replay on top of recording.

# Pseduo code:

## on launch
	load litert
	download/load posenet model
	main activity with buttons.

## main activity:
	load pose button
		- pre generate pose data files.
		- option to explore user downloaded/recorded pose data files; select and load.
	capture button
		- one time camera capture [photo] - covert to pose data
	record/stop button
		- continuous camera capture [video] - covert to pose data [with time series]
	save button
		- save pose data to file ;  to db
	share button
		- share pose data over bt.

## on exit
	free resources.


# Languages
 * english

