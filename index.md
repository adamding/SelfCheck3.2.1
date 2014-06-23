---
title       : Self-Check Questions (ungraded)
subtitle    : Discrete vs. Continuous pdf
author      : Aidong Adam Ding
job         :  Made using Slidify in R. (Click mouse then right arrow key for next slide.)
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : solarized_dark      # 
widgets     : [mathjax, quiz, bootstrap]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides

--- &radio

## Question 1: 

X has pdf $f(x)=0.1x,\quad x=1,1.5,3,4.5$. 

Which of the following answer equals to $P(1 \lt X \leq 4.5)$?

1. $\int_1^{4.5} {0.1xdx}$
2. f(1)+f(2)+f(3)+f(4)
3. 0.1+0.2+0.3+0.4 
4. $\int_{1.5}^{4.5} {0.1xdx}$
5. f(1.5)+f(2.5)+f(3.5)+f(4.5) 
6. _f(1.5)+f(3)+f(4.5)_
7. f(1)+f(1.5)+f(3)+f(4.5) 

*** .hint
This is a discrete random variable. So you need to find the case satisfies $1 \lt X \leq 4.5$, then add up the probabilities of those cases, 

*** .explanation
There are three cases satisfies $1 \lt X \leq 4.5$: X=1.5, X=3 and X=4.5. 

f(1.5)+f(3)+f(4.5) is the sum of the probabilities of three cases.

--- &multitext

## Question 2

X has pdf  $f(x)=x^2/338350,\quad x=1,2,...,100$. 

1. What is the P($10 \leq X \lt 50$)?

*** .hint
Is this a discrete or continuous random variable? 

You will need to either sum or integrate over the range of possible values.

*** .explanation
1. <span class="answer">0.1186</span>

This is a discrete random variable. You need to add up the probabilities of those cases satisfies $10 \leq X \lt 50$. That is, the cases X=10, X=11, ., X=49. (X=50 not included due to the "$\lt$" sign). 

Use R command to find: 

sum((10:49)\^2/338350)

--- &radio

## Question 3
Which of the following is indeed a pdf?

1. $f(x)=0.0625(x^2-2),\quad x=-3,-2,0,2,3$ 

2. $f(x)=0.0625(x^2-2),\quad 2 \lt x \lt 4$

3. $f(x)=(x^2-2)/6,\quad -3 \lt x \lt 3$

4. $f(x)=0.0625(x^2-2),\quad x=-3,-2,2,3$

5. _$f(x)=(x^2-2)/57,\quad 3 \lt x \lt 6$_

*** .hint
Check if the function satisfies the two properties on the range of possible values: 

(1) always nonnegative; (2) P(S)=1.

*** .explanation
Only the last one is a real pdf.

1. $f(x)=0.0625(x^2-2),\quad x=-3,-2,0,2,3$ contains negative f(0)= -0.125; 

2. $f(x)=0.0625(x^2-2),\quad 2 \lt x \lt 4$, P(S) does not equal 1; 

3. $f(x)=(x^2-2)/6,\quad -3 \lt x \lt 3$ contains negative f(x), e.g., f(0)=-1/3; 

4. $f(x)=0.0625(x^2-2),\quad x=-3,-2,2,3$, P(S) does not equal 1. 




