---
layout: post
title:  "Multiple Of"
date:   2018-08-18 07:00:00 -0700
category: [blog, challenge]
---

<iframe width="100%" height="475" src="https://dotnetfiddle.net/Widget/2XtcdT" frameborder="0"></iframe>

<a href="https://github.com/jacobschellenberg/MultiplesOf" target="_blank">View on GitHub</a>

First of all, if you know a clean way to convert `GetSumOfMultiplesOf` into a more functional... function, I'd appreciate the pro tip.

I also couldn't think of a better name for the variables `_multipleOf01` and `_multipleOf02`. It's might be slightly confusing that you are getting the multiple of `01` or `02`, but the name is supposed to represent the input, of which there are 2.

Apparently I wrote the initial version of this back in November 2013. Nearly 5 years ago.

Looking back at it, I was pretty happy with the result. When I wrote this, I would have been a fresh graduate from college, only a few months out.

I decided to upload this one first because, well, I'm just going through all my projects in alphabetical order, cleaning them up, and uploading them here for posterity.

I just wanted to note that this is my current coding style. I'm sure I'll end up doing a post purely about coding style/standards. I've spent a lot of time pondering, studying, and devising coding styles.

I hope this tiny bit of code is a good representation of my own personal, clean coding standards.

The only thing I'm not too happy about here is the function `GetSumOfMultiplesOf` because of the mutation of the `sum` variable. Otherwise, the non-mutation of the `sumOfMultiples` is pretty darn neat.

I'm really trying to be more functional in my programming. It's getting there!