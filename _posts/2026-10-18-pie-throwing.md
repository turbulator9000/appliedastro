---
title: pie throwing
tags: [math]
---

> what is an ankle in 3D
>
>-Salem Sehiri, 2026

This first for real post is not about my integration bee or math website progress since I am quite sick right now and waiting until I can like fully get a routine before I start grinding. This post is about something I learned in my discrete lecture I thought was interesting and kind of funny because really only mathematicians could think up these kinds of problems.

## the pie throwing problem

Imagine this scenario: there are **an odd number** of people, pies in hand, **all different distances away from each other**, ready to throw at the **person nearest to them**. Prove that there is always one person who isn't hit by pie.

## solution

This is a very awesome usage of mathematical induction: if you prove that a base case is true, then assume the statement is true for some positive integer $$k$$ and use it to prove that its also true for some next step $$k+1$$, then the statement is true for all positive integers. If that's confusing, this example is perfect to get started.

### base case

Let's start with the base case of **3** people, since **1** person can't really have a pie fight without it being really sad, and 3 is the next positive odd number. 

Since they are all at different distances from each other, there are two people whose closest person is each other. The only way this would not be true is if all three people were equally distanced from eachother in an equilateral triangle. Let's call these two Will and Salem, and the other Eddie. 

![before the pie]({{ site.baseurl }}/assets/beforepie.png)

So Will throws at Salem and Salem throws at Will. Eddie throws at whoever is closest to him, so it could be either Will or Salem, but he **does not get any pie thrown at him**. So we've proven our base case for $$n=3$$ people.

![after the pie]({{ site.baseurl }}/assets/afterpie.png)

### induction step

Let's just do one step up and see how we can generalize downwards from there. Imagine **5** people now. Two pairs of people throw pie at each other because they are each other's closest person. That leaves one person left unpied. Imagine **7** people, so now there are three pairs of people who throw pie at each other leaving one person unpied. This goes on and on for 9 people, 11 people, so on and so forth. So its true!!

#### this is where you skip if you could care less

Formally, lets say there are $$2k+1$$ people (that is how you write an odd number formally), and that this theory that one person will not be hit is always true for $$2k+1$$ people. So we want to show that this is also true for $$2(k+1)+1 = 2k+3$$ people.

Imagine Will and Salem again in these $$2k+3$$ people. They are each others closest person, so they throw at each other. Now remove them from the pool: $$2k+3-2 = 2k+1$$. Since we assumed this is true for the $$2k+1$$ people remaining, it must be true! 

Induction is like dominos: if we know/assume that the first domino is going to knock over the second, and the second knocks over the third, then we know that the third is going to knock over the fourth, and so on and so forth (bars). It might seem circular a bit but it works because of something called the **well-ordering principle**, which you could look up on your own time. Very cool.

Just thought this was a neat little way to introduce induction. Love.

