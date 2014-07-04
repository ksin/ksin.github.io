---
layout: post
title:  "DBC Final projects | part two"
date:   2014-07-04 08:15:00
categories: dbc final-project
---

Happy July 4th! I'm actually pretty happy it's a holiday at DBC today. Not only is the school empty, quiet, and void of distracting activities, the train I took this morning was equally serene. We won't have Sam and Rebecca around to answer our questions, but in exchange, I think we'll get a lot of space to focus 100% on our project today. Sam said we can Snapchat him any questions we had. We'll see about that.

Yesterday, I started by converting all the schemas we drew into models. I had written around 20 tests when Rebecca and Sam came in for our consultation. Rebecca gave us some really good advice on prioritizing features, and offered us a different perspective on how we should approach each sprint so that we can have an MVP ready on time. Rather than spending a lot of time setting up for everything we planned to do, we should only implement the small chunk of things that'd make our app work minimally at the first iteration. Then every iteration afterwards should be a fully working feature, ones that are immediately important to the app's concept. This all seems logical now, but we certainly needed someone like Rebecca to shift our perspective.

From there, we re-organized our Trello board, and re-prioritized our features to sooner realize the true utility of the app. In the end, we came to a clearer understanding of what really makes our app an improvement over GoodReads. Personally, I think it helped us break each sprint into real, presentable features, so that come Thursday, we can't possibly be stuck in the middle of implementing a feature and realize we're in a rabbit hole. Of course, I had to dump all the tests I wrote because now we were only creating models as they were necessary for features. 

We came across our first few hurdles last night, particularly when dealing with OAuth. Firstly, Dave and I couldn't figure out how to write feature tests for OAuth -- frankly, controller tests for OAuth was tough too. We did some research for about an hour. We seeked Sam and Rebecca's help and they gave us a few suggestions. Rebecca reminded me that we should just try all the methods we thought of, instead of immediately searching for the bestest way to do things. Sometimes, the best way to do things isn't clear, and we will have to tinker around to find out. In the end, we decided to timebox these tests since the cost of figuring out how to write them was way more than the support they provided. Essentially, we laid trust in GoodReads to send the user to the right page after authenticating, and decided we can verify it with our own tests later if we had the time.

The next problem we encountered was actually implementing the log in with OAuth. That was Judy's task. Sessions were not storing objects the way we had expected. We couldn't figure out why our code wasn't working despite it being configured just like all the other examples we had seen. It took awhile and a bit of panicking, but eventually, Judy figured a work around that involved reconstructing the request token in the callback. This may be a surprisingly good method too, as now we store less in the session between authentication actions, and we also bypass possible browser incompatibilities.

Luckily, Raghav's job was to implement the home page for a guest user, so it didn't clash with any of our code. No problems there. However, we ran into some Travis CI problems. Turned out our build was failing. We fixed it by around 10 PM. BUT THEN, I checked Travis again just now and it turned out it wasn't fixed. I did some changes and made a pull request before starting this blog post (since builds take, like, foreverrr). Let's check it out now...

![passedtravis](/assets/passedtravis.png)
![17tests](/assets/17tests.png)

We didn't complete as many tasks as we expected today, but I think today was a particularly tough one. I did notice a little more swearing from everyone today. :P 

Now that we got the OAuth done, I think we'll really start rolling. We may be a little slower than other groups because of the time we spent optimizing our testing environment, but I think setting up properly, will make our lives easier in the long run.

Our first sprint ends today, which means Judy buys us ice cream. :) 

![sprint1calendar](/assets/sprint1calendar.png)

I still think there's a better way for us to divide the work to be more efficient. For one, I guess we need to lax up on the commit and pull request standards we set for ourselves so we can get more work done. I will propose my other ideas to the team today and we'll see how things work out by tomorrow. Bye for now.