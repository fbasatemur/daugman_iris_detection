# Daugman's algorithm for Iris detection


The Daugman algorithm is a commonly used method for iris and pupil detection. The algorithm analyzes the pixel data in the image to determine the iris and pupil regions, based on the principle of enclosing the iris pattern with a circular boundary.


[UBIRIS.v1](http://iris.di.ubi.pt/ubiris1.html) 200x150 grayscale data has been used as the test dataset. 

<img src="https://github.com/fbasatemur/daugman_iris_detection/blob/main/images/sample.png" alt="eye_img" height="225" width="300">

## Daugman Integrodifferential Operator

<img src="https://github.com/fbasatemur/daugman_iris_detection/blob/main/images/daugman_operator.png" alt="eye_img" height="180" width="700">

Explanation of the equation:

I(x,y) : The value of the pixel at coordinates (x,y)

![integral](https://latex.codecogs.com/svg.latex?\color{white}\int_{r,x0,y0}^{}\frac{I(x,y)}{2\pi.r}dx)  : The operation calculates the area for a circle with radius r and centered at (x0, y0).

![türev](https://latex.codecogs.com/svg.latex?\color{white}\frac{d}{dr}) : The operation represents the difference or derivative between the fields.

G(r): It is the Gaussian operator that is multiplied to ensure that the differences between the fields follow a normal distribution.

The max operation is used to capture the circle with radius r centered at (x0, y0) that has the maximum derivative transition

Sources:
- [How Iris Recognition Works -- John Daugman](https://www.robots.ox.ac.uk/~az/lectures/est/iris.pdf)
- [UBIRIS.v1](http://iris.di.ubi.pt/ubiris1.html)


