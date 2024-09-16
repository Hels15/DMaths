---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
permalink: /DifferentialEquations
---
# First-Order Linear Equations

A first-order differential equation is one that can be written in the form:

$$ \frac{dy}{dx} + P(x)y = Q(x)$$

A **linear function** is a function whose graph is a polynomial function of degree **zero** or **one**.

For example, a polynomial of degree **zero** is:

![Polynomial of degree zero](https://via.placeholder.com/400x400?text=Graph+of+f(x)=2)

A function with degree **one** is also a linear function.

![Polynomial of degree one](https://via.placeholder.com/400x400?text=Graph+of+f(x)=2x%2B1)

From this, we can conclude that these functions are defined in terms of \( x \), which is raised either to power **one** or **zero**.

Similarly, a linear equation is an equation in which the highest power is always **one**.

**First order** means (a polynomial of degree at most one).

A differential equation is an equation involving the derivative(s) of the dependent variable (\textbf{y}) with respect to the independent variable (\textbf{x}).

We see that:

\[
\frac{dy}{dx}
\]

is just the derivative of the dependent variable with respect to the independent variable.

We see that:

\[
P(x), Q(x)
\]

both define functions in terms of \( x \). For example:

\[
P(x) = kx^0, \quad Q(x) = 0x^{0}
\]

\[
kx^0 = k \cdot 1 = k
\]

respectively:

\[
0x^0 = 0 \cdot 1 = 0
\]

Since any functions of \( x \) satisfy the general form, we can rewrite it such that:

\[
\frac{dy}{dx} - ky = 0
\]

Here:

\[
k = P(x), \quad 0 = Q(x)
\]

This shows how:

\[
k = P(x), \quad 0 = Q(x)
\]

can be used as an alternative form meaning the same thing.

**Example 1: Putting the equation in standard form**

\[
x \frac{dy}{dx} = x^2 + 3y, \quad x > 0
\]

**Solution**

\[
\begin{aligned}
x \frac{dy}{dx} &= x^2 + 3y \\
\frac{dy}{dx} &= x + \frac{3}{x}y \\
\frac{dy}{dx} - \frac{3}{x}y &= x
\end{aligned}
\]

## Solving Linear Equations

Solving linear equations means that we solve the equation for \( y \).

**Example 2: Simple differential equation**

\[
y' + \frac{1}{x}y = 2
\]

We can rewrite this such that:

\[
y'x + y = 2x
\]

Can we solve this equation for \( y \) **explicitly**? So that we get \( y \) on one side and some expression on the other side. We can't, since the differential equation is not separable.

> **Note:** A separable equation is solved by separating the variables, that is rearranging the equation so that everything involving \( y \) appears on one side of the equation, and everything involving \( x \) appears on the other.

However, we can solve the equation by noticing that the equation can be written in the form:

\[
xy' + y = 2x
\]

We can also see that this is just the product rule with respect to \( x \):

\[
\frac{d}{dx}[xy] = \frac{d}{dx}[x]y + \frac{d}{dx}[y]x
\]

Since:

\[
\frac{d}{dx}[x]y + \frac{d}{dx}[y]x = xy' + y = (xy)'
\]

We can also see that:

\[
(xy)' = 2x
\]

Our only goal is to find the value of \( y \). To get rid of the derivative, we can do the inverse operation (take the integral):

\[
xy = x^2 + C \quad \text{or} \quad y = x + \frac{C}{x}
\]

Here, we didn't need to use any formulas, we just simply rearranged the equation and recognized the product rule so that the equation could be solved for \( y \). **Note** that \( C \) represents the constant of the equation, thus leading us to a general solution.

**Example 3: Why do we need the constant?**

The reason why we need the constant is that the integral of a derivative can lead to multiple correct answers. Think about it this way:

\[
\frac{d}{dx}[x + 1] = 1
\]

\[
\frac{d}{dx}[x + 2] = 1
\]

Now, if we take the integral of these results we should arrive back to the original function. In other words, this is our expectation:

\[
y = x + 1
\]

\[
\frac{dy}{dx} = 1
\]

\[
\int 1 \, dx = x
\]

As it turns out, this is ambiguous - there are more than one functions that, when taking the derivative, result in **1**. This means that the input for the integral will be the same even if the original functions differ.

\[
y = x + 2
\]

\[
\frac{dy}{dx} = 1
\]

\[
\int 1 \, dx = x
\]

Here, both the functions \( f(x) = x + 1 \) and \( f(x) = x + 2 \) will end up the same after integration, but we know they are **not the same**. If the integral is supposed to show the area under a specific curve, surely it should output 2 different values since the area is unique to the curve itself.

**Links for the graphs:**

- [x + 1](https://www.desmos.com/calculator/yhl4sxh0a0)
- [x + 2](https://www.desmos.com/calculator/itwb1c7klv)

> **Note:** \( C \) is an arbitrary constant meaning that any value of \( C \) would make \( F(x) + C \) a valid antiderivative.

This is the reason why we include the arbitrary \( C \) - to show that it differs by some constant. The arbitrary constant \( C \) can be dropped if there is an initial condition - or if the integral is **between boundaries**.

\[
\int x + 2 \, dx = \frac{x^2}{2} + 2x + C
\]

This is called the general solution. To find a precise value for \( C \), an initial condition can be defined.

## Initial Value Problems

\[
\int dy = \int f(x) \, dx \quad \Rightarrow \quad y = F(x) + c \quad \leftarrow \text{general solution}
\]

**Example 4: Initial Value Problem**

\[
(t^2 - 3t + 2) \frac{dx}{dt} = 1 \quad (t > 2), \quad x(3) = 0
\]

First we have to understand why this is an initial value problem - initial value problems always include an initial condition. An initial condition **specifies the value** of the unknown function at a given point in the domain.

\[
x(3) = 0
\]

In other words:

\[
\text{when } x = 3, \; y = 0
\]

The function **returns zero** when the input is **3**. We can also examine the domain restriction placed on the problem:

\[
(t > 2)
\]

This just simply states - **t** must be greater than 2 in order to have a well-defined function. Notice how plugging in **2** to:

\[
(2^2 - 3(2) + 2) = 0
\]

gives us **zero**. Once we understand what an initial condition is, we need to talk about what kind of differential equation we are dealing with. Going back to the original example:

\[
(t^2 - 3t + 2) \frac{dx}{dt} = 1 \quad (t > 2), \quad x(3) = 0
\]

We can recognize this as a separable differential equation. They are defined in the form:

\[
N(y) \cdot \frac{dy}{dx} = M(x)
\]

In our case, **y** can be replaced with **t** as we are working with functions defined in terms of **t**. The reason why we call them *separable* is that they can be separated in a way so that each of the sides only contains functions defined in terms of themselves.

\[
N(y) \cdot dy = M(x) \, dx
\]

Taking the integral:

\[
\int N(y) \cdot dy = \int M(x) \, dx
\]

will give us the solution.

**Worked Solution 1:**

\[
(t^2 - 3t + 2) \frac{dx}{dt} = 1 \quad (t > 2), \quad x(3) = 0
\]

\[
(t^2 - 3t + 2) \frac{dx}{dt} = 1
\]

\[
\frac{dx}{dt} = \frac{1}{t^2 - 3t + 2}
\]

\[
dx = \frac{1}{t^2 - 3t + 2} \cdot dt
\]

\[
\int dx = \int \frac{1}{t^2 - 3t + 2} \, dt
\]

\[
x = \frac{1}{(t-1) \cdot (t-2)}
\]

\[
\frac{1}{(t-1) \cdot (t-2)} = \frac{A}{t-1} + \frac{B}{t-2} \quad \text{(partial fractions)}
\]

\[
1 = A(t-2) + B(t-1)
\]

\[
1 = (A + B)t - (2A + B)
\]

\[
A + B = 0 \quad \text{so} \quad B = -A
\]

\[
-2A - B = 1
\]

\[
-2A - (-A) = 1
\]

\[
-2A + A = 1
\]

\[
-A = 1
\]

\[
A = -1 \quad \text{and} \quad B = 1
\]

\[
x = \int \left(\frac{-1}{t-1} + \frac{1}{t-2}\right) \, dt
\]

\[
x = -\ln |t - 1| + \ln |t - 2| + C
\]

\[
x = \ln \frac{t-2}{t-1} + C
\]

Using the initial condition, we can obtain the real result:

\[
t = 3, \quad y = 0
\]

\[
0 = \ln \left|\frac{3-2}{3-1}\right|
\]

\[
0 = \ln \left|\frac{1}{2}\right|
\]

\[
-\ln \left|\frac{1}{2}\right| = \ln 2
\]

Since:

\[
a \ln(b) = \ln (b^a) \quad \text{so} \quad -\ln \left(\frac{1}{2}\right) = \ln \left(\frac{1}{2}^{-1}\right) = \ln 2
\]

## Linear ODE

At the beginning of Chapter 9, we started off with this form:

\[
y' + P(t)y = g(t)
\]

However, instead of providing a way of dealing with these questions immediately, we looked at how these questions can be solved in other ways. See: Separable equations, product rule, etc. Now we introduce an algorithm that works when we have a differential equation in the above form.

**Example 5: Linear ODE**

\[
x \cdot \frac{dy}{dx} + 2y = 1 - \frac{1}{x}, \quad x > 0
\]
