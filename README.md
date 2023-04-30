Download Link: https://assignmentchef.com/product/solved-homework-3-cpsc-475-beng-475
<br>
For this assignment, note that parts 1 , 2 , and 3 are <strong>optional</strong>, and are meant to help building a better understanding of the material and studying for the exams. Parts 4 and 5 are worth 15% and 85%, respectively. Make sure to include the code for your functions in your write-up!

<h1>Linear independence and basis</h1>

1a Consider the vectors <strong>u </strong>= [1 1]<em><sup>T </sup></em>and <strong>v </strong>= [3 −1]<em><sup>T</sup></em>. What is the result of the expression <em>α</em><strong>u </strong>+ <em>β</em><strong>v </strong>if <em>α </em>= 2 and <em>β </em>= 1<em>.</em>5? Is this a linear combination? Why or why not?

b Find the scalars <em>α</em><sup>0 </sup>and <em>β</em><sup>0 </sup>that make the following expression true: <em>α</em><sup>0</sup><strong>u</strong>+<em>β</em><sup>0</sup><strong>v </strong>= [4 8]<em><sup>T</sup></em>.

c Express the equation above in matrix form and compute <em>α</em><sup>0 </sup>and <em>β</em><sup>0 </sup>using MATLAB/Python. Hint: this involves creating a matrix from <strong>u </strong>and <strong>v </strong>and computing its inverse.

d Now consider the following 2 vectors in R<sup>3</sup>: <strong>x </strong>= [1 1 − 1]<em><sup>T </sup></em>and <strong>y </strong>= [1 − 1 − 1]<em><sup>T</sup></em>.

Are they independent? Why?

e Find scalars <em>α </em>and <em>β </em>such that <em>α</em><strong>x </strong>+ <em>β</em><strong>y </strong>= [1 0 2]<em><sup>T</sup></em>. Do <strong>x </strong>and <strong>y </strong>form a basis for R<sup>3</sup>? Why or why not?

f Consider the following 3 vectors: <strong>x </strong>= [1 0 0]<em><sup>T</sup></em>, <strong>y </strong>= [1 − 1 − 1]<em><sup>T </sup></em>and <strong>z </strong>= [0 3 − 1]<em><sup>T </sup></em>Are they orthogonal to each other? Do they form a basis for R<sup>3</sup>? Why?

g Consider the column vectors in the 3 × 3 identity matrix. Do they form a basis for R<sup>3</sup>? Is this an orthogonal basis? Why? Express the vector [2 1 7]<em><sup>T </sup></em>as a linear combination of these column vectors — by which scalars do we need to multiply each of them?

h Now consider the vectors <strong>u </strong>= [1 1]<em><sup>T </sup></em>and <strong>v </strong>= [1 − 1]<em><sup>T</sup></em>. Do they form a basis for R<sup>2</sup>? If yes, can you make it into an ortho<strong>normal </strong>basis?

i Consider the vector <strong>x </strong>= [−1 3]<em><sup>T </sup></em>(which basis is it in, by the way?). Find the scalar coefficients <em>α </em>and <em>β </em>needed to express <strong>x </strong>in terms of the orthonormal basis from h . Hint: you can find the coefficients in the form of a vector [<em>α β</em>]<em><sup>T </sup></em>using the same approach as in c !

<h1>Intro to Fourier series</h1>

2a Compute <em>y</em><sub>1 </sub>= sin(<em>t</em>) using MATLAB/Python and make a plot of the values in y1. Note that, in order to see the sinusoidal curve, <em>t </em>must be an array, t. It should contain a range of values so as to include one complete period, i.e., [0<em>,</em>2<em>π</em>] (using linspace is a good idea). Choose a small step size between each value in t so that the curve appears relatively smooth (if you’re using linspace, that is equivalent to choosing a large number of points – at least 1000 for best results).

b Using the same t as above, compute <em>y</em><sub>2 </sub>= sin(2<em>t</em>) and plot it on top of y1<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>. Now compute the result of sum(y.*y2) (or np.sum(y*y2) in Python). Using a new figure, repeat this procedure for <em>y</em><sub>1 </sub>and <em>y</em><sub>3 </sub>= sin(3<em>t</em>). What do you notice about the results?

c What is the dot product between y1 and y2? Can we say sin(<em>t</em>) is orthogonal to sin(2<em>t</em>)? Can y1 and y2 be seen as functions of <em>t</em>? Can they be seen as vectors? Explain. Repeat the experiment using each of the following two pairs: <em>y</em><sub>2 </sub>and <em>y</em><sub>3</sub>; <em>y</em><sub>1 </sub>and cos(<em>t</em>).

Comment briefly on the results. d Using the same t as above, plot the function <em>w </em>= 3cos(5<em>t</em>)+7cos(15<em>t</em>)+1<em>.</em>2cos(30<em>t</em>).

e Compute the dot product between <em>w </em>and the following vectors: <em>y</em><sub>1</sub>, <em>y</em><sub>2</sub>, and <em>y</em><sub>3 </sub>(from above), as well as <em>y</em><sub>5 </sub>= cos(5<em>t</em>), <em>y</em><sub>−5 </sub>= cos(−5<em>t</em>), <em>y</em><sub>15 </sub>= cos(15<em>t</em>), <em>y</em><sub>−15 </sub>= cos(−15<em>t</em>), <em>y</em><sub>30 </sub>= cos(30<em>t</em>), and <em>y</em><sub>−30 </sub>= cos(−30<em>t</em>). Always divide your results by <em>n</em>, the length of your vector t. What do you observe?

f If you created a “basis” formed by the vectors above (<em>y</em><sub>1</sub><em>,y</em><sub>2</sub><em>,y</em><sub>3</sub><em>,y</em><sub>−5</sub><em>,y</em><sub>5</sub><em>,y</em><sub>−15</sub><em>,y</em><sub>15</sub><em>,y</em><sub>−30</sub><em>,y</em><sub>30</sub>),

what would be the scalar coefficients needed to express <em>w </em>in terms of that basis?

g Now, compute the discrete Fourier transform of your signal w using the function fft; use fftshift<a href="#_ftn2" name="_ftnref2"><sup>[2]</sup></a> to translate the zero-frequency to the middle of the spectrum, followed by abs/np.abs to compute the magnitude of the complex values obtained—you can do all of this using a single line of code: W = abs(fftshift(fft(w))). Now make sure to divide W by n (the length of your t vector) and plot it against its corresponding frequency values, f—this is the vector containing the range of values -n/2:n/2-1 (in Python, this range is equivalent to np.arange(-n/2,n/2)), i.e., the maximum frequency will be half of the sampling rate of your discrete signal (does the name Nyquist come to mind??).

Execute plot(f,W) and either zoom in or set xlim(-50,50) to have a better look at the peaks in your plot<a href="#_ftn3" name="_ftnref3"><sup>[3]</sup></a>: what do they represent? How do their frequency and magnitude values relate to the equation for <em>w</em>? How does this relate to what you did in f ? Finally, what would you expect to happen to your frequency plot if we changed the coefficients 3, 7, and 1.2 in the equation for <em>w </em>to different values? What if we changed the frequencies 5, 15, and 30 to different values?

h Now increase the number of periods in t to at least four (if <em>T </em>is the number of periods you choose, your new range for the values in t should be [0<em>,</em>2<em>πT</em>]). Let w = sawtooth(t, 0.5)<sup>4 </sup>(a triangular wave) and examine its plot: what can you say about this function? How is it different from the sum of sinusoidals you investigated above? Is it still periodic?

Continuous? Smooth?

Compute its discrete Fourier transform and compare it with what you got above. In particular, what can you say about the frequency distribution? Note: this time, to the get correct frequency values, you must divide the frequency scale by number of periods chosen above

(T).

i Finally, repeat this procedure for w = sawtooth(t) (a sawtooth wave). What is different now? Is it still periodic? Continuous? Smooth? What do you notice about its frequency spectrum?

<h1>Computing discrete convolution</h1>

3a Inside the following boxes are the impulse responses of a few linear systems. Manually (on paper!) compute the output of each system given its input signal (left column). Assume the grids below represents integers centered at (0<em>,</em>0). Apply your computations only to the integer points, i.e. a discrete convolution. Check your answers against the results returned by running conv/np.convolve on MATLAB/Python, but first make sure you understand the difference between the three possible modes of convolution: ‘full’,’same’, and ‘valid’.

Ask us if you don’t know how.

b Now you will compute 2-D discrete convolution. On the left is a 2-D input array, and on the right the impulse response (“kernel”) of a linear system. The gray square represents the center (origin) of the kernel. Compute the (full) 2-D convolution between the two (pad with 0s as necessary) and check your result against running conv2/scipy.signal.convolve2d. (Hint: here, because the signals are two-dimensional, you need to flip them both vertically and horizontally before sliding!)

<h1>Fourier Transform and convolution with images</h1>

In this problem set, we will examine filters and their Fourier transforms. In class, we discussed an expansion of functions into a basis of sines and cosines. Recall from class that one could take the dot product of two functions <em>f </em>and <em>g </em>as follows:

Z h<em>f,g</em>i =  <em>f</em>(<em>x</em>)<em>g</em>(<em>x</em>)<em>dx.</em>

Therefore, we can think of expanding a function into sines and cosines much like expanding a vector onto an orthogonal basis. Let <em>f</em><sup>ˆ</sup><sub>sin</sub>(<em>ω</em>) = <sup>R </sup><em>f</em>(<em>x</em>)sin(<em>ωx</em>)<em>dx </em>be the sine expansion of the function <em>f </em>and <em>f</em><sup>ˆ</sup><sub>cos</sub>(<em>ω</em>) = <sup>R </sup><em>f</em>(<em>x</em>)cos(<em>ωx</em>)<em>dx </em>be the cosine expansion, where <em>ω </em>is the angular frequency. Then, using Euler’s formula (<em>e<sup>iθ </sup></em>= cos<em>θ </em>+ <em>i</em>sin<em>θ</em>), the Fourier transform of the function <em>f </em>is: Z

<em>f</em>ˆ(<em>ω</em>) = <em>f</em>ˆcos(<em>ω</em>) + <em>if</em>ˆsin(<em>ω</em>) =         <em>f</em>(<em>x</em>)<em>e</em>−<em>iωx </em><em>dx</em>

(the negative sign in the exponent is simply a convention!).

4a<strong>* </strong><em>Prove </em>that ) where <em>f</em>∗<em>g </em>is convolution. In other words, that the

Fourier transform of a convolution is the product of the Fourier transforms of the functions.

Feel free to do this on paper and attach it to your write-up.

5a<strong>* </strong>Write a function that creates a Gaussian blur filter (flesh out the code in blurfilter.m/py).

Your function should create a matrix <em>M </em>(called filt in the code), where

<em>.</em>

Use the matrices xs and ys provided in blurfilter (e.g., xs(i,j) contains the <em>x<sub>ij </sub></em>component that should be used in the expression above)<a href="#_ftn4" name="_ftnref4"><sup>[4]</sup></a>. Normalize the sum of the entries to one by dividing by the sum of the entries. Why is this last step desired?

b<strong>* </strong>Using fft2, compute the 2-dimensional Fourier transform of a filter created using your function from a with <em>σ </em>= 1, and display the absolute value of the transform (abs function) using surf(···, ‘EdgeColor’, ‘none’) (plot surface in Python). What (familiar function) does the Fourier transform of this filter look like? (Hint: Use fftshift to properly center your transformed image in the <em>ω<sub>x </sub></em>and <em>ω<sub>y </sub></em>directions.)

The appearance of the filter transform can be improved by adding padding to your FFT by using fft2(filter, pady, padx) (in Python, fft2(filter, (pady,padx))) where pady and padx are larger than your filter’s vertical and horizontal dimensions, respectively.

c<strong>* </strong>Load the Paolina image (remember to convert it to double precision numbers in the range [0<em>,</em>1]!). Filter Paolina (convolve using mode ‘same’) with a blur filter having <em>σ </em>= 3 and display the result. <strong>Compare </strong>this with computing the inverse Fourier transform (ifft2) of the pointwise product between the Fourier transforms of Paolina and your filter (compute the transforms of the filter and the image, separately, then compute the inverse transform of the product of the two transforms). Be sure to pad the fft2 of Paolina and the fft2 of your filter to the same size (larger than the image—ideally, equal to Sp + Sf – 1 along each axis, where Sp and Sf are the sizes of Paolina and the filter along each axis, respectively.

How does this relate with what you showed in 4a ?

d<strong>* </strong>Using your function from a , build a 13×13 Difference of Gaussians filter, with <em>σ</em><sub>1 </sub>= 1 and <em>σ</em><sub>2 </sub>= 2. In other words, build a 13×13 matrix containing the pointwise difference of two Gaussian filters, the first having <em>σ</em>-parameter <em>σ</em><sub>1 </sub>and the second having <em>σ</em>-parameter <em>σ</em><sub>2</sub>, with <em>σ</em><sub>2 </sub><em>&gt; σ</em><sub>1 </sub>. Normalize this filter so that the sum of its entries is zero, by subtracting the mean of the entries of this matrix. Apply this filter to Loki.tiff and Steve.tiff, displaying the result using imagesc/plt.imshow with a gray colormap. How does this filter affect features in the image?

e<strong>* </strong>Compute the 2-dimensional Fourier transform of this filter and display it. Why is this considered to be a band-pass filter? (Note: Once again you should use fftshift to shift the

Fourier-transformed image.)

f<strong>* </strong>Flesh out the code in unsharpmask.m to create a function that performs unsharp

masking on an input image. Unsharp masking an image consists of three steps:

<ol>

 <li>Blurring the image;</li>

 <li>Subtracting the blurred image from the original image to create the “mask”;</li>

 <li>Scaling the mask by some amount and adding it back to the original image.</li>

</ol>

Use the function to perform unsharp masking on Paolina.tiff with the parameters sigma = 1 and amount = 1 (although feel free to experiment!). Compare the filtered images to the original images (this time, use imagesc(···,[0 1]) or plt.imshow(···, vmin=0, vmax=1) in Python). Describe what the unsharp mask filter appears to be doing to the image.

<a href="#_ftnref1" name="_ftn1">[1]</a> in MATLAB, use the hold on command after plotting y

<a href="#_ftnref2" name="_ftn2">[2]</a> in Python, both functions can be imported from the numpy.fft submodule.

<a href="#_ftnref3" name="_ftn3">[3]</a> you can also play with xticks to customize the frequency values shown along the x-axis in your plot. <sup>4</sup>in Python, import the sawtooth function from scipy.signal.

<a href="#_ftnref4" name="_ftn4">[4]</a> note that this means you can use the power of elementwise operations to compute all <em>M<sub>ij </sub></em>entries in a single line of code using xs and ys directly!