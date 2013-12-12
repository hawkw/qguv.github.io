---
layout: post
title: "Syntax Highlighting Test"
date:   2013-12-12 16:15:00
categories: test code programming
---

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

