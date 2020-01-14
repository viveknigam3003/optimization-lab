# Linear Programming Guide
The following is meant to be performed in MuPAD application for MATLAB R2015b.

## Maximize and Minimize

Syntax:
```MATLAB
linopt::minimize([{<constraints>}, <objective function>])
linopt::maximize([{<constraints>}, <objective function>])
```
For Example:
```MATLAB
linopt::minimize([{c1 + c2 <= 6, c2 <= 15}, -c1 - c2])
```
This will return - `[OPTIMAL, {c1 = 0, c2 = 6}, -6]`

To plot the same thing <br>
Syntax:
```MATLAB
k := [{<constraint>}, <obj function>]:
g := linopt::plot_data(k, [x, y]):
plot(g):
```
