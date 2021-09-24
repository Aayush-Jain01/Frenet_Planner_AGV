Splines
=======
A spline is an aggregation of several piecewise functions that is used to fit a smooth curve(approximately) passing through several vector/data points.

Splines provide smoothness and control which makes them such a useful and important interpolation technique in practical scenarios where we want smooth shapes and estimations to our data

One such class of Splines "Cubic Splines" are used in our code

Key Properties of Cubic Splines
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
1. They are continuous at the merging/control points

2. They have continuous first and second derivatives at the points where they join 


Calculating A Cubic Spline 
^^^^^^^^^^^^^^^^^^^^^^^^^^
A cubic spline is basically made up of piecewise cubic polynomials each satisfying the interval and the endpoints of the interval they are defined in.

Let's say there are n + 1 points (x0, y0), (x1, y1), (x, y2) ....... (xn, yn)

We want to fit a cubic spline through these n+1 points or we can say that we need to find n cubic equations that make up the spline iver these n-intervals 

Any cubic equation passing through a point x_i, y_i can be written in the form :-

y_i = a + b(x - x_i) + c(x-x-i)² + d(x-x_i)³

Here we have 4 unknowns for one cubic equation.So for n cubic equations we will have 4n unknowns

As cubic splines satisfy certain properties, these serve as constraints for the unknowns 
