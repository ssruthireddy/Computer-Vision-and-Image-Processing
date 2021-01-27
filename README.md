# Computer-Vision-and-Image-Processing
Computer Vision and Image Processing

Computer Vision and Image Processing
•	Computer Vision and Image Processing
o	Image Processing 
  Detection
  Segmentation
  localisation
  recognisation fo objects in images
  evaluation of results
  Tracking an object
  Activity Classification
  Object Categorization
  Scene Categorization

o	Image Features
  	The Most raw feature in an Image is Pixel- Pixel intensity values
  	0 means = Black
  	255 means = White
  	But then we certainly normalise, when we normalise values are in the range of 0 to 1.
o	Image can be represented as a function
  	Image Transformations like - Increase the brightness, - Flip the image along an axis
  
o	3 Image Processing Operations
	1.Point : performing point opeartion on that point to get corresponding output
  	Reverse the contrast
  	Histogram equalization to stretch the contrast
  	One of the uses is to reduce the noise
	2. Local: performing opeation on surrounding and neighbour pixels aswell, take average of all pixels
	3. Global:  output of specific co-oridnate is independent on all values in input image
o	Noise Reduction: 
  	Moving Average: replace each pixel by avg of its neighbour pixels
  1D - sgnals, speech, sound
  2D Moving Average
o	Filter / Kernel / Mask - all mean same
	Smoothing Filters
	Linear Filter/Mean Filter/Box filter
  	Amount of blur depends on filter size
  	Box like appearance would be visible in the filtered image. Hence we look into Gaussian filter.
	Gaussian Filter
  	 Amount of blur depends on the variance value & filter size
  	Central pixel is given highest weightage, neighbouring pixels are given high importance & diagonal neighbours are given least weightage
	Properties of smoothing filters
  	All value should be positive
  	Sum of all values should be = 1
	Sharpening Filter 
	(Brightening Filter - Smoothing Filter)
	Combination of filters give rise to new filters
	Edge Detectors 
	Edges are formed at a place where we have maximum change in intensity values between pixels
  	Origins of edges
  	Surface color / appearance discontinuity
  	Depth discontinuity
  	Illumination discontinuity
  	Surface normal discontinuity
	Sobel Edge detectors 
  	Sobel along X-axis 
  	Detect vertical edges
  	Sobel along Y-axis
  	Detect horizontal edges
	Prewitt
  	Finds vertical or horizontal edges
	Roberts
  	Edges along diagonals
  	Orientation angle of edge
  	tan inverse of (partial derivative along y / partial derivative along x)
  	Reduce the noise in detecting edges

	Improvised version of steps
  	1. Take the input image
  	2. Take the derivative of gaussian filter
  	3. Convolve the result of step 2 on input image
	Canny Edge Detector – Optimal edge detector
	Steps
  	Good Detection: Filter responds to edge not noise
  	Good Localisation: Detected edge near true edge
  	Single Response: One line per edge (for this people do non-maximum suppression) per edge step - 3.
  	1. Apply Sobel along X-axis & Sobel along Y-axis
  	2. Combine the results of Sobel along X & Y-axis
  	3. Non-maximum suppression(to avoid thick edges)
  	To ensure that we get a single edge
  	4. Apply Hysteresis Thresholding
  	Min
  	Max
	Laplacian Filter 
	Blob Detection
	Laplacian of Gaussian
	Second derivative of Gaussian Filter
	Non Linear Filter
  	Median Filter to reduce the noise
	Bilateral Filter 
  o	Cross-correlation & Convolution - Sicle image gets fliped from both the sides, people has stopped using cross co-relation and started using convolution.
  
o	Boundary Effects
  	Padding
  	Zero
  	Wrap
  	Clamp
  	Mirror

o	Sampling and Interpolation
	Sub-Sampling
  	Image Aliasing 
	Nyquist Rate

	Wagon-wheel effect 
  	Sub sampling with Gaussian Filter
  	Apply Gaussian filter on the image & then subsample
	Image Pyramid/Gaussian Pyramid 
	Gaussian pre-filtering
	Upsampling
   Image Interpolation
  	Increase the size of the image
  	Nearest Neighbor Interpolation 
  	Linear Interpolation 
  	Bi-Linear Interpolation 
  	Bicubic Interpolation 
  
o	Practical World using OpenCV library
  	Read, View, Save the images
  	Converting images from one color space to another
  	Splitting the various color channels & combining the color channels
  	Image Translation, Rotation, Scaling, Affine & Projective transformations
  	Detecting human face & human body parts
  	Haar Cascades
  	Seam Carving
  	Removing or Adding uninteresting points to downsample or upsample the image

