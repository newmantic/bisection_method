# bisection_method


The Bisection Method is a numerical technique for finding the root of a continuous function. A root of a function f(x) is a value x such that f(x) = 0. The Bisection Method works by repeatedly narrowing down an interval [a, b] that contains the root.


Intermediate Value Theorem:
If a function f(x) is continuous on the interval [a, b] and f(a) and f(b) have opposite signs, then there exists at least one root c in the interval [a, b] such that f(c) = 0.
This theorem is the foundation of the Bisection Method

Interval Selection:
Start with an initial interval [a, b] where the function changes sign:
f(a) * f(b) < 0
This ensures that a root exists within the interval.

Iteration Process:
Compute the midpoint c of the interval:
c = (a + b) / 2
Evaluate the function at the midpoint f(c).
If f(c) = 0, then c is the root.
If f(a) * f(c) < 0, the root lies in the left subinterval [a, c], so update b = c.
If f(b) * f(c) < 0, the root lies in the right subinterval [c, b], so update a = c.
Repeat the process until the interval [a, b] is sufficiently small.

Convergence:
The Bisection Method is guaranteed to converge to a root, provided that the function is continuous and the initial interval satisfies f(a) * f(b) < 0.
The method converges linearly, meaning that the error (distance between the midpoint and the root) decreases by half with each iteration.


Pseudocode

Input: Function f(x), interval [a, b], tolerance epsilon.
Check: Ensure f(a) * f(b) < 0.

While (b - a)/2 > epsilon:
Compute the midpoint:
c = (a + b) / 2
Evaluate f(c).
If f(c) = 0, return c as the root.
If f(a) * f(c) < 0, update b = c.
If f(b) * f(c) < 0, update a = c.

End While
Output: The root is approximately (a + b)/2.

