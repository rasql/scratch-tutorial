Techniques
==========

This section shows useful programming techniques.

Click on blocks to execute 
--------------------------

You can click on blocks in the palette and on blocks on the canvas and execute these blocks.
For exemple you could click on these **move** and **turn** blocks to test them.

.. image:: block1.png

Running block is yellow
-----------------------

When your block is running, it has a yellow outline.
You can start the **forever** block by clicking on it.
When you click a second time, it stops.

.. image:: block2.png

Stack blocks
------------

You can stack blocks. Clicking on any of the blocks, will execute the whole stack.

.. image:: block3.png

Capitalize sprite names
-----------------------

Capitalize sprite names. They are classes from which you can clone objects.

.. image:: sprite1.png

Sprites have variables
----------------------

Sprites have built-in variables, which describe their state.
You can visualize these **reporters** by checking them.

.. image:: var1.png

This makes the values be displayed on the stage.

.. image:: var2.png

Click on reporters
------------------

Click on a reporter block to display it's value.

.. image:: var3.png

Sprite variables
----------------

Each sprite (and clone) has these variables:

- position (x, y)
- visible
- size
- direction

.. image:: sprite2.png

Toggle size
-----------

When toggling a value, you need a variable to store the current state. 
You can use existing variables. In the following example the size variable is used to toggle.

.. image:: size1.png


Change size by
--------------

We can show the effect of the **change size by** block
by applying it in a loop on multiple clones of the cat.

.. image:: size2.png

Inside the loop we:

- create a clone
- move by 80 points
- change the size by 10

The first 4 cats are clones, the last one is the orignal.

.. image:: size3.png

Increment a variable
--------------------

The block **change by** can be used to increment a variable.
The exemple below increments the variable **i** by 1 when pressing space.

.. image:: inc.png

We display the variable in a speech bubble.

.. image:: inc2.png

Reset the counter
-----------------

Each time we press the space bar the counter **i** increments.
We can add an **if** block to reset the counter when reaching a certain value.

.. image:: inc3.png

Use modulo to wrap
------------------

Another way to wrap around is the function **modulo** or **mod** which returns
the remainder of a division.

This is shorter:

.. image:: mod.png

How does it work ? 
You can place only the **mod** block on the programming canvas and test it
by entering numbers and click with the mouse to evaluate the expression.

You will see **5 mod 6** is 5 (the reminder of 5 divided by 6).

.. image:: mod2.png

You will see **6 mod 6** is 0 (the reminder of 6 divided by 6).

.. image:: mod3.png

The counter i cycles through the 6 values 0, 1, 2, 3, 4, 5.

To start with 1 instead with 0 we can modifiy the expression to this.

.. image:: mod4.png

The counter i cycles now through the 4 values 1, 2, 3, 4.

Cycle the other way
-------------------

We can also decrement and cycle back when reaching 0.

.. image:: mod5.png

Here the counter **i** cycles through the range 3, 2, 1, 0.

