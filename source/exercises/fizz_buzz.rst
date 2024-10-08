.. _exercise_fizz_buzz:

##################
Fizz Buzz Exercise
##################

Fizz Buzz is a classic simple problem in computer science.

It is often used as an exercise in interviews for programmers.

Apparently a LOT of people applying for jobs as professional developers can't do this in an interview: http://c2.com/cgi/wiki?FizzBuzzTest

Now that we've psyched you out, know that it's really pretty straightforward.

Goal
====

* Write a program that prints the numbers from 1 to 100 inclusive.
* But for multiples of three print "Fizz" instead of the number.
* For the multiples of five print "Buzz" instead of the number.
* For numbers which are multiples of both three and five print "FizzBuzz" instead.

Hint
====

Look up the ``%`` operator. What do these do?

* ``10 % 7``
* ``14 % 7``

Try those in iPython.

**Do** try to write a solution *before* looking it up. There are a million nifty solutions posted on the web, but you'll learn a lot more if you figure it out on your own first.

Results
=======

Running your code should result in something like::

    1
    2
    Fizz
    4
    Buzz
    Fizz
    7
    8
    Fizz
    Buzz
    11
    Fizz
    13
    14
    FizzBuzz
    16
    ....
