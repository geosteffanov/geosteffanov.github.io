---
layout: post
title:  "From NAND 2 Tetris: Basic Logic Gates"
date:   2016-06-11 18:23:00 +0200
categories: coding
future: true
published: true
use_math: true
---

## Wut iz dis? ##

The first and most basic principle in computer architecture is that of the logic gates.
It is not the 'physical' aspect of computers: using electricity and transistors - in theory nothing stops you from creating a computer using ants, or maybe people, fluids or something else you can predictably control, just as long as it has the capacity to represent two different basic values, which we can call *true* and *false*. Well, strictly speaking, electrical computers may be the most efficient right now, but this is out of my range of knowledge, so I have to keep an open mind about it.

It turns out two different values: true and false, 1 and 0, on and off, cats and dogs, are enough to represent all of the logic a computer uses.

Remarkably, through the use of scaling, abstraction and layering, very small pieces of 'computers' are needed to eventually build the real thing.

## Logic ##

Some of you may be familiar with elementary math logic, and some of you may not, so I will give a small example, before we continue:

<!-- Some examples of AND, OR and NOT -->

So, really, what we're talking about here are functions - things that take values and output values accordingly (computers do exactly that). Our functions will take values that can either be 1(true) or 0(false). From here on, we will use 1 for true, and 0 for false - this will make things easier in the future. These functions will also output such values. Such functions we call _boolean_.

It can be shown, that the following statement is true: 

<!-- all boolean functions of n variables are 2^2^n -->

As a result, one only needs a finite set of boolean functions of n variables to represent any one boolean function of n variables. At the very least, you can take all the 2^2^n functions.

But there is a stronger statement:

<!-- All boolean functions of n variables can be formed with the use of only not, and and or functions -->

That's interesting.. Only 3 functions are enough to represent any one boolean function? But wait, there's more:

<!-- Show Nand function, and that it can simulate not, and and or -->

So, we've come to the following conclusion:

Every boolean function can be simulated using only the NAND function. It is hard to realize how powerful this statement is. So consider this:

## Logic Gates ##

Imagine we can successfully implement a NAND function in real life. If we have a machine that takes two inputs, both possibly one of two values (1 or 0), does something internally and then outputs again a value that represents 1 or 0, in a way that that value is the NAND of the inputs, then we will be able to connect in some way multiple copies of this machine to make arbitrary boolean functions.

Enter the NAND gate - a device that really does the above. It is called a gate, because when two signals (naturally, of type 1 or 0) pass through it, what comes out on the other side is their NAND.

<!-- Show some explanation -->

Without going into details, imagine the NAND gate as a black box, from which 3 pins protrude - two input ones, and one output pin. These pins can be connected to other pins, which has the effect of creating a path through which boolean signals can pass and transform. Because we can fanout a pin (make it go in several directions at once), we can feed the same pin in the two input pins of a nand gate. This is equivalent to creating the NOT of the signal.
With some careful planning and trial and error, you can convince yourself that in this way we can make arbitrary functions.



## So how are logic gates, boolean functions and computers related? ##

Computers use electrical signals to do their magic. Although they are of course not only in one of two states, either 1 or 0, but rather they continously flow from one to the other, there are ways around that which allows us to implement NAND gates, through the use of transistors for computers to use. Logic gates are a way of encapsulating and abstracting the implementation of the NAND, AND, OR, etc. They are a natural 'predecessors' of chips - which use several logic gates interconnected in a way so that they perform some expected functionality.


## Wrapping things up ##
As we shall see further into the series of posts, even though construction of logic gates is simple, carefully calculated combinations of the basic NAND gate leads to the complex, and even more versatile computer.



**_If something in this post doesn't seem right to you, or is outright wrong, please feel free to tell me - if you'd like so, your name might appear on a contributor list on the site. Additionally, I will learn from my mistake and will ofcourse correct it. In a way, we both gain something from this. I apologize in advance for any such mistakes._**





