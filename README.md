# Integral-Pi
Approximating Pi by solving an integral

The basis of this algorithm is this equation:
$$\frac{\pi}{4} = \int\limits_0^1 \sqrt{1-x^2} dx$$
This integral is approximated using slicing. There is a variable called ```area```. Its value is 1, which is the area of one slice that covers the entire integral (1x1 area). At each iteration, slices are doubled, and the total area of the slices decrease, approaching $\frac{\pi}{4}$. The change in area is subtracted from ```area```.

This algorithm is recursive. It can be presented with math using summation notation as:
$$\frac{\pi}{4} = 1 - \sum\limits_{i=1}^{\infty} \Bigg( \sum\limits_{j=0}^{2^{i-1}-1} \frac{ \sqrt{1 - (\frac{2j}{2^i} )^2 } - \sqrt{1 - (\frac{2j+1}{2^i} )^2 } }{2^i} \Bigg) $$
