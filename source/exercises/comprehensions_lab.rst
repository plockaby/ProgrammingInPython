.. _exercise_comprehensions:

##################
Comprehensions Lab
##################

Goal
====

Getting familiar with list, set and dict comprehensions.

List Comprehensions
--------------------

Note: this is a bit of a "backwards" exercise. We show you code and then you figure out what it does.

As a result, there is not much to submit. Don't worry about it. You'll have a chance to use these in other exercises.

.. code-block:: python

    >>> feast = ['lambs', 'sloths', 'orangutans',
                 'breakfast cereals', 'fruit bats']

    >>> comprehension = [delicacy.capitalize() for delicacy in feast]

What is the output of this?

.. code-block:: python

    >>> comprehension[0]
    ???

    >>> comprehension[2]
    ???

Figure it out before you try it.

Filtering Lists With List Comprehensions
----------------------------------------

.. code-block:: python

    >>> feast = ['spam', 'sloths', 'orangutans', 'breakfast cereals',
                'fruit bats']

    >>> comp = [delicacy for delicacy in feast if len(delicacy) > 6]

What is the output of this?

.. code-block:: python

    >>> len(feast)
    ???

    >>> len(comp)
    ???

Figure it out first, before trying!

Unpacking Tuples in List Comprehensions
---------------------------------------

.. code-block:: python

    >>> list_of_tuples = [(1, 'lumberjack'), (2, 'inquisition'), (4, 'spam')]

    >>> comprehension = [ skit * number for number, skit in list_of_tuples ]

What is the output of this?

.. code-block:: python

    >>> comprehension[0]
    ???

    >>> len(comprehension[2])
    ???

Double List Comprehensions
---------------------------

.. code-block:: python

    >>> eggs = ['poached egg', 'fried egg']

    >>> meats = ['lite spam', 'ham spam', 'fried spam']

    >>> comprehension = \
    [ '{0} and {1}'.format(egg, meat) for egg in eggs for meat in meats]

What is the output of this?

.. code-block:: python

    >>> len(comprehension)
    ???

    >>> comprehension[0]
    ???

Set Comprehensions
------------------

.. code-block:: python

    >>> comprehension = { c for c in 'aabbbcccc'}

What is the output of this?

.. code-block:: python

    >>> comprehension
    ???

Dictionary Comprehensions
-------------------------

.. code-block:: python

    >>> dict_of_weapons = {'first': 'fear',
                           'second': 'surprise',
                           'third':'ruthless efficiency',
                           'forth':'fanatical devotion',
                           'fifth': None}
    >>> dict_comprehension = \
    { k.upper(): weapon for k, weapon in dict_of_weapons.items() if weapon}

What is the output of this?

.. code-block:: python

    >>> 'first' in dict_comprehension
    ???
    >>> 'FIRST' in dict_comprehension
    ???
    >>> len(dict_of_weapons)
    ???
    >>> len(dict_comprehension)
    ???

Other Resources
---------------

See also:

https://github.com/gregmalcolm/python_koans/blob/master/koans/about_comprehension.py

From Greg Malcolm's excellent Python Koans series:

https://github.com/gregmalcolm/python_koans

Count Even Numbers
------------------

This is from CodingBat "count_evens" (http://codingbat.com/prob/p189616)

*Using a list comprehension*, return the number of even integers in the given list.

Note: the % "mod" operator computes the remainder, e.g. ``5 % 2`` is 1.

.. code-block:: python

    count_evens([2, 1, 2, 3, 4]) == 3

    count_evens([2, 2, 0]) == 3

    count_evens([1, 3, 5]) == 0

Can you do this with a single line comprehension?

.. code-block:: python

    def count_evens(nums):
       one_line_comprehension_here

``dict`` and ``set`` Comprehensions
-----------------------------------

Revisiting the dict/set lab, see how much you can do with comprehensions instead: :ref:`exercise_dict_lab`

Specifically, look at these:

First a slightly bigger, more interesting, or at least bigger, dict:

.. code-block:: python

    food_prefs = {"name": "Chris",
                  "city": "Seattle",
                  "cake": "chocolate",
                  "fruit": "mango",
                  "salad": "greek",
                  "pasta": "lasagna"}

Working With This dict
----------------------

1. Print the dict by passing it to a string format method, so that you get something like:

    "Chris is from Seattle, and he likes chocolate cake, mango fruit, greek salad, and lasagna pasta."

2. Using a list comprehension, build a dictionary of numbers from zero to fifteen and the hexadecimal equivalent. String is fine. The ``hex()`` function gives you the hexidecimal representation of a number as a string.

3. Do the previous entirely with a dict comprehension. This should be a one-liner.

4. Using the dictionary from item (1), make a dictionary using the same keys but with the number of 'a's in each value. You can do this either by editing the dict in place, or making a new one. If you edit in place make a copy first!

5. Create sets s2, s3, and s4 that contain numbers from zero through twenty, divisible 2, 3 and 4.

    a. Do this with one set comprehension for each set.

    b. What if you had a lot more than 3? -- Don't Repeat Yourself (DRY).

        - Create a sequence that holds all the divisors you might want. It could be 2,3,4, or could be any other arbitrary divisors.

        - Loop through that sequence to build the sets up -- so no repeated code. You will end up with a list of sets -- one set for each divisor in your sequence.

        - The idea here is that when you see three (Or more!) lines of code that are almost identical, then you you want to find a way to generalize that code and have it act on a set of inputs, so the actual code is only written once.

    c. For extra credit, do it all as a one-liner by nesting a set comprehension inside a list comprehension. (OK, maybe this is getting carried away!)
