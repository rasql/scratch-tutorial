Pen
===

The pen extension is a drawing module.
It adds 9 dark green blocks.

.. image:: pen_blocks.png

The pencil sprite
-----------------

We are going to use the **Pencil** sprite. 
In order to make the line appear at the point of the pencil, 
you must go to the sprite editor, select the whole drawing (cmd+A) 
and place the tip of the pencil at the origin marker.

.. image:: pen_sprite.png

Draw a line
-----------

Now we can place the pencil somewhere on the stage and draw a line.
To do so we:

- erase all
- set the pen color (red)
- set the pen size (3 points)
- put the pen down
- move 100 steps

.. image:: pen_move.png

This is the result, drawn on the backdrop with xy axes.

.. image:: pen_move2.png

Move slowly
-----------

The **Motion** category has a **glide to x, y** block.
We can create a similar block for gliding a certain distance.

In Scratch a loop executes 25 times each second.
To last **t** seconds, it must repeat **tx25** times.

The distance increment of each iteration is **1/(tx25)** of the total distance.

.. image:: pen_glide.png

To test the gliding move we write:

.. image:: pen_glide2.png

Turn slowly
-----------

Now let's write a block which rotates the sprite slowly.

.. image:: pen_turn.png

Let's test it.

.. image:: pen_turn2.png

Draw a square
-------------

Now we combine the slow move and the slow turn block to draw a square.

.. image:: pen_square.png

This is the result.

.. image:: pen_square2.png

Draw a polygon
--------------

We can turn this into a function **polygon** which can draw any arbitrary regular polygon.

.. image:: pen_polygon.png

This is the code to test for a hexagon.

.. image:: pen_polygon2.png

This is the result drawn to the stage.

.. image:: pen_polygon3.png

Draw a star
-----------

There is a simple algorithm to draw a star. 
It's almost like a polygon, but it has an extra parameter **m**.

- n : the number of points
- m : the number of points to jump over

.. image:: pen_star.png

This is the result for a **(7, 3)** star which is a 7-pointed star, 
jumping always to the 3rd point.

.. image:: pen_star2.png

Here is the code:

.. raw:: html

    <iframe src="https://scratch.mit.edu/projects/397107138/embed" 
    allowtransparency="true" width="485" height="402" frameborder="0" scrolling="no" allowfullscreen></iframe>

https://scratch.mit.edu/projects/397107138 

Store points in a list
----------------------

In the following section we look at a technique to store points in a list.
For this we need to define 3 variables:

- **x, y** the 2D coordinates
- **i** an integer index which points to the current point in the list

.. image:: pen_var.png

Then we create a list called **Points**. 
This list contains the coordinates of all the points of the shape.

The image below shows the **Points** list with the points (0, 0), (100, 0) and (100, -50).
They represent a rectangular triangle. The first point is repeated at the end to close the shape.

.. image:: pen_points.png

We define a fonction **set x, y** to add the point (x, y) to the **Points** list.

.. image:: pen_set.png

The functiion **Triangle** sets the 4 points of the triangle shown above.

.. image:: pen_triangle.png


Load and store
--------------

Operations are executed using two variables **x** and **y**.
At any time, the index variable **i** points at a pair of coordinates in the list.

The **load** function loads the coordinates (x, y) from the **Points** list to the variables.

.. image:: pen_load.png

The **store** function transfers the coordinates (x, y) from the variables back to the **Points** list.

.. image:: pen_store.png

Draw a shape
------------

The **draw** function does the following

- set the index **i** to the first point
- repeat for each point
- load the current point to the variables **x** and **y**
- go to position (x, y)
- put the pen down
- increment index **i** by 2

.. image:: pen_draw.png

Translate a shape
-----------------

The function **add** adds the vector (x, y) 
to the point currently pointed to by the index **i**.

.. image:: pen_translate.png

The function **translate** does this for every point in the **Points** list.
It also draws the shape.

.. image:: pen_translate2.png

Now we can apply the translation to the triangle.

.. image:: pen_translate3.png

This is the result.

.. image:: pen_translate4.png


Scale a shape
-----------------

The function **mul** multiplies the point currently pointed to by the index **i**
with a scalar value **k**. A positive angle turns counter-clockwise.

.. image:: pen_scale.png

The function **scale** does this for every point in the **Points** list.
It also draws the shape.

.. image:: pen_scale2.png

Now we can apply the scaling to the triangle.

.. image:: pen_scale3.png

This is the result.

.. image:: pen_scale4.png


Rotate a shape
-----------------

The function **rot** rotates the point currently pointed to by the index **i**
by an angle **a**, with reference to the origin.

.. image:: pen_rotate.png

The function **rotate** does this for every point in the **Points** list.
It also draws the shape.

.. image:: pen_rotate2.png

Now we can apply the rotation to the triangle.

.. image:: pen_rotate3.png

This is the result.

.. image:: pen_rotate4.png

Translate, scale and rotate
---------------------------

Now we define a slighly more complex L-shape.

.. image:: pen_L.png

We applay successively a

- translation
- scaling
- rotation

.. image:: pen_L2.png

This is the result:

.. image:: pen_L3.png

This is the project

.. raw:: html

    <iframe src="https://scratch.mit.edu/projects/398912533/embed" 
    allowtransparency="true" width="485" height="402" frameborder="0" scrolling="no" allowfullscreen></iframe>

https://scratch.mit.edu/projects/398912533



