---
layout: post
title: "Doing well on hackathons: LauzHack case study"
description: "Doing well on hackathons: LauzHack case study"
keywords: "Hackathons, LauzHack, LauzHack 2.0, python, programming, hack"
---

This is a quick post about various hackathon tips that can be helpful for people doing hackathons for the first time, and how these tips applied to us at [LauzHack 2.0](http://lauzhack.com/). I've done a couple (5 to be precise) of hackathons, and while I didn't get anything at the first two, I got some prizes at each of the last three.

So just in case you don't know, [Hackathon](https://en.wikipedia.org/wiki/Hackathon) is programming event/competition where you engineer something under time constraints (typically 1 day) and demo it afterwards for a chance to win some prizes. We'll define "doing well" as building something interesting, learning something new and getting some prizes.

Last weekend I participated in [LauzHack 2.0](http://lauzhack.com/) hackathon in a team of 3 and we ended up doing pretty well there - we got a runner-up spot overall plus a Logitech prize. We've built a system that allows to manipulate your computer using gestures captured by a web camera, see [Iron Man Manipulator](https://devpost.com/software/iron-man-manipulator) for a longer description. It had a couple of extra features for a nice demo and was built using python+OpenCV.

![](https://github.com/maksay/lauzhack/raw/master/maksai.jpg)
*Andrii using our project*

<div class="divider"></div>

Let's begin with my hackathon tips.

**#1**: the first step to doing well is getting a good team. A "good team" doesn't mean that there has to be [Jeff Dean](https://research.google.com/pubs/jeff.html) in it, but rather that you are comfortable working with each other. For some projects it's a good bonus if you have a diverse set of skills (e.g. a front-end person and a back-end person), or if you have overlaps in some areas and can help each other with the difficulties. The latter is pretty important - your problem is entire teams problem, so you should be collaborative in solving issues. Because of all this I think that it's better to make a team with your friends. However, at LauzHack 2.0 we ended up going to a competition as a team of 2, so Andrii (my teammate) decided to look for an extra person. We found Mihail - a Moldovian guy studying in Germany, who, just like me and Andrii, is a competitive programmer. We ended up collaborating quite well, with each of us writing a significant portion of the code.

**#2**: pick a good idea. This depends on a type of hackathon you're attending - sometimes you're asked to build something that can become a startup (so you have to think about the business side of the pitch), or focus on technology with no powerpoint crap, which was the case at LauzHack. Typically a good idea involves:
1. using a trendy method or device (e.g. VR, machine learning or Alexa)
2. having a good demo potential (saying that your music recommender app only works for 1000+ users is VERY bad)
3. having a simple practical use-case. Last year winnner is a great example of this - they build a mobile app for tracking washing labels once you cut them off, uing computer vision usage to read label info.

You don't have to be perfect at all 3 - for example our solution lacked a practical use-case (but made up for it with technical complexity and a nice demo). Or there was a simple social-media blocker app, which had a practical use-case and a nice UI. I would also mention that novelty is often overrated - truly new ideas are VERY rare. So it's OK to build yet another voice assistant, but ideally it should have some distinctive feature that well-known ones don't have (e.g. setting humor level like TARS in "Interstellar").

**#3**: Come up with a tentative plan and check-up on the actual progress every hour or so. A rule of thumb for new engineers is to multiply their estimate of feature completion time by 2. For hackathons, you should also divide the number of planned features by 2 :) Account for extra time when dealing with new technologies - your first step should be to get some simple examples working on your machine. Definitely start from the most important features and if there are multiple parts of technology stack, try to parallelize the work (don't spend first 1/2 of time on frontend only to discover that you can't finish backend in time). You should be code complete ~2 hours before the deadline and save that time for polishing (~1 hour will go into pitch preparation). Don't make major changes in the last minutes - in 99% of cases that's a bad decision!

Quick anecdote from LauzHack: none of us had extensive experience with OpenCV (although we had some), so the first thing we did is got simple examples working. Took us a bit of time to get it working on Mihail's ubuntu, where pip opencv package missed camera support (me and Andrii use OS X). Afterwards, we discovered a funny bug, where the camera video feed stops after 100 seconds. There is a 2 year github thread with dozens of people confirming this bug, with the only fix being "go to this C++ file, change this line of code and recompile OpenCV". Nobody ever merged this fix into a new OpenCV version. So we just made sure that our demos are less than 100 seconds - nobody wanted to mess with OpenCV source code. As a young student I thought that top-notch open source projects are made by really smart people, but after seeing various open-source code during industry work, and writing some myself, I can safely say that it's often quite bad :)

**#4**: Write the code "smartly". The core part of the hackathon is spent writing code, so it helps if you can do that well :) There are several tips related to writing hackathon code versus industry or homeworks. First of all, nobody is going to read your code, so as long as you can understand it, you can do whatever you want - use global variables, have [spaghetti code](https://en.wikipedia.org/wiki/Spaghetti_code) and other things that are unacceptable by the sane people. Second, it is OK to use "dirty" workarounds - for example I couldn't figure out how to pass input to a lua tool called Hammerspoon programmatically, so I just made it read the input from a text file each 0.1 second, while my program was updating contents of that file. This is bad engineering, but works flawlessly for a hackathon. Lastly, one programming principle you should **\*not\*** ignore is modularity. You are writing this project as a team, so it helps a lot for you to define APIs beforehand, and then for each team member to implement her/his part. For example, in our project Andrii wrote a function that computed hand location, with me and Mihail using it to update slider and button values. As a result, we had no issues with merging our code or compatibility between different parts of code. 

**#5**: Spend the last hour polishing your demo and pitch. While you can create the best project ever, if you cannot showcase it well, you won't get the prizes. Thus, prepare a demo and practice your pitch in front of your teammates. It helps to have a memorable pitch - one that produces "wow!" effect or makes your audience laugh (this is true for most presentations). I probably did a mediocre job with pitching our project, but still, I'm much better at that than I once was. I'll attribute this to the fact that Eastern European high schools place 0 emphasis on learning how to present/speak well, unlike their North American counterparts. Luckily, public speaking, like many other things, can be learned.

<div class="divider"></div>

So that's about it. Follow these 5 tips and you have a decent chance to build something cool and get some prizes. It's worth mentioning that out of 5 hackathons I've been to, LauzHack had the best prizes and swag - kudos to the organizers and sponsors!

![](/assets/images/prizes.png)

^ Prizes each of us got. 
