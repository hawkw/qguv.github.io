---
layout: post
title: "Syntax Highlighting Test"
date:   2013-12-12 16:15:00
author: Quint
authorlink: http://lmgtfy.com/
vim: si:et:ts=2:sw=2
category: test
tags:
- test
- code
- programming
---

I am testing the text feature now.
Our neural pathways have become accustomed to your sensory input patterns. Sure. You'd be surprised how far a hug goes with Geordi, or Worf. Computer, belay that order. Shields up! Rrrrred alert! Wait a minute - you've been declared dead. You can't give orders around here. Fate. It protects fools, little children, and ships named "Enterprise." Talk about going nowhere fast. In all trust, there is the possibility for betrayal. Your head is not an artifact! Fear is the true enemy, the only enemy. They were just sucked into space. We could cause a diplomatic crisis. Take the ship into the Neutral Zone Sorry, Data. When has justice ever been as simple as a rule book? We have a saboteur aboard. But the probability of making a six is no greater than that of rolling a seven. Smooth as an android's bottom, eh, Data? I can't. As much as I care about you, my first duty is to the ship. I suggest you drop it, Mr. Data. Yes, absolutely, I do indeed concur, wholeheartedly! I am your worst nightmare! I've had twelve years to think about it. And if I had it to do over again, I would have grabbed the phaser and pointed it at you instead of them. I guess it's better to be lucky than good. And blowing into maximum warp speed, you appeared for an instant to be in two places at once. Well, that's certainly good to know.

{% highlight python3 linenos %}

import math
from rpcalc.inout import clear

class Stack:
    '''
    An implementation of the RPN stack in Python3.
    Internally uses a list and negative indexes.
    '''

    def __init__(self, initList, name, limit=None):
        self.items = initList
        self.name = name
        self.limit = limit

    def __len__(self):
        return len(self.items)

    def __str__(self): #ref: len
        rep = self.name
        if self.name != '': rep += '\n'
        if self.limit:
            rep += "limited to " + str(self.limit) + " entries\n"
        backList = [ self[i] for i in range(len(self)) ]
        if len(self) != 0:
            longestEntry = max( [ len(str(i)) for i in self.items ] )
        else:
            longestEntry = 3
        rep += '--' * int(math.floor(longestEntry / 2 + 1)) + '-'
        rep += '\n'
        for i in range(len(self.items)):
            rep += ' '
            rep += str(self.items[i])
            rep += '\n'
        rep += '\n'
        rep += '^ ' * int(math.floor(longestEntry / 2 + 1)) + '^'
        #looks like entry point
        return rep

    def linearView(self): #ref: getitem, len
        backList = [ self[i] for i in range(len(self)) ]
        print(str(backList))

{% endhighlight %}

I am testing the text feature now.
Our neural pathways have become accustomed to your sensory input patterns. Sure. You'd be surprised how far a hug goes with Geordi, or Worf. Computer, belay that order. Shields up! Rrrrred alert! Wait a minute - you've been declared dead. You can't give orders around here. Fate. It protects fools, little children, and ships named "Enterprise." Talk about going nowhere fast. In all trust, there is the possibility for betrayal. Your head is not an artifact! Fear is the true enemy, the only enemy. They were just sucked into space. We could cause a diplomatic crisis. Take the ship into the Neutral Zone Sorry, Data. When has justice ever been as simple as a rule book? We have a saboteur aboard. But the probability of making a six is no greater than that of rolling a seven. Smooth as an android's bottom, eh, Data? I can't. As much as I care about you, my first duty is to the ship. I suggest you drop it, Mr. Data. Yes, absolutely, I do indeed concur, wholeheartedly! I am your worst nightmare! I've had twelve years to think about it. And if I had it to do over again, I would have grabbed the phaser and pointed it at you instead of them. I guess it's better to be lucky than good. And blowing into maximum warp speed, you appeared for an instant to be in two places at once. Well, that's certainly good to know.

