# Plot_ly_surface.io

## Overview

As part of the Developing Data Products course, I created a simple webpage with R Markdown that features an interactive Plotly plot. In this case, it is a sine wave as a 3D surface.

## Interactive Plotly Plot
```{r}
library(plotly)
x <- seq(-10, 10, length.out = 100)
y <- seq(-10, 10, length.out = 100)
z <- outer(x, y, function(x, y) sin(sqrt(x^2 + y^2)))
plot_ly(z = ~z, x = ~x, y = ~y, type = "surface")
```
