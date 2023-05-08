Download Link: https://assignmentchef.com/product/solved-steady-state-temperature-in-a-thin-metal-plate
<br>
1) Steady State Temperature in a Thin Metal Plate

Imagine a thin metal plate surrounded by heat sources along each edge, with the edges held at different temperatures. After a short time, the temperature at each location on the plate Will settle into a steady state. This can be modeled by dividing the plate into a discrete grid of cells and simulating the change in temperature of each cell over time:

100

90

90

90

80

100

712,1)

100

711,2)

100

711,3)

712,3)

113,3)

100

95

95

95

At each time step, the temperature m each interior cell (i,J) will be the average of four of its surrounding

neighbors:

<ol>

 <li>a) Part 1</li>

</ol>

Develop a program to determine the steady state temperature distribution in the plate by representing the plate  as a two-dimensional array with NROWS rom and NCOIß columns. NROWS and NCOLS should be declared as global constants (suggestiom use 20 for both valtrs).

Your program should do the following:

Declare 2 separate two-dimensional arrays named temp and 0ld. Array 0ld Will be used to

maintain the current values Of the grid temperatures and array temp Will be used to compute the new

values obtained at each successive time step using the equation above.

prompt the user and enter temperature values for the top, bottom, left, right sides. Also prompt and

enter an initial temperature T(ij) for the interior cells. (For this lab, you may initialize all the interior

cells to a Single, user-input temperature)

Initialize temp using these values and display the initial contents Of the temp array on the console.

Obtain a convergence criterion from the user (say, 0.001)

Use a convergence loop to continue updating the t emp array until the temperature in every cell con-

verges using the following method:

<ol>

 <li>Set a boolean variable named steady to true</li>

 <li>Copy temp to old</li>

 <li>Loop overall the interior cells (but not the edge cells!)</li>

</ol>

– [3-1]


temp

If I temp til —oldtil &gt; convergence_criterion,

then set steady to false

Repeat this 3 -step process again and again until all the cells simultaneously satis$ the convergence

This is a longer program than usual, so here are a number of hints;

<ul>

 <li>Before writing any code think about what the code should look like: what will an outline look Will</li>

</ul>

it involves loops? If so. how many. where. and of

<ul>

 <li>what type? Will there be if statements? If so. where and how many? what variables Will your program need to keep track Of Which Of these Will be arrays?</li>

</ul>

Think about these questions and discuss them with your partner before actually writing any code.

<ul>

 <li>Write, test, and debug your code incrementally, rather than all at once.</li>

</ul>

Create a function named void display (double temp [J [NCOLSI) . You can use this function

to print out that array at any time , and so the function will be useful in debugging your program

<ul>

 <li>Make sure you can explain tie difference between the old array and the temp array, and</li>

 <li>why your pro- gram needs to use both</li>

 <li>Make sure you understand how to have your program loop through only the interior Of the array.</li>

 <li>Make sure you understand what the convergence criterion test is, and what role it plays you program.</li>

</ul>




<ol>

 <li>b) Part 2 (optional)</li>

</ol>

Now you will visualize the steady state temperature data by creating a 3D plot using Matlab. Begin by modifying your program so that the final temperature data is written to a file named temp. dat instead of (or in

addition to) the terminal screen. Then open Matlab by typmg the followmg commands:

*module load math/matlab

*mat lab

When the application opens, move the cursor to the Command window and enter the following Matlab

commands in order and observe What happens:

nrows = 20

ncols

(x, y) — meshgrid(l:nrows,l:ncols)

load temp-dat

mesh (x, y, temp)

surf (x, y, temp)

The mesh function produces a mesh or wireframe plot Of the data. The surf function produces a surface plot.

Try using the rotate button from the menu bar to have a good look at die data’