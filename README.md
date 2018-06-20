# imagecollage
This is Project 1 From Computer Vision Grad Course Offered at ITU Lahore.

Problem 01

Create a color version of image shown in Figure 1.
Write a function that goes through each pixel of the input image (using for loop) and output colored
version of it. Since we are going to from less information to more information, we have to define rulesor mapping from gray scale to the RGB color. (Reference images could be found from here
http://www.tayloredmktg.com/rgb/).
If the input image’s (x,y) pixel is white and y being row is less than 7
o Output image should have sky blue color at (x,y) location.
if the input image’s (x,y) pixel is white and y being row is Greater than or equal to 7
o Output image should have pink color at (x,y) location.
If the pixel is gray
o Output image should have Moccasin at (x,y) location.
Otherwise makes it White
Remember don’t change your input image but the output image only. You can use ‘imwrite’ for write
the image to the file. Submit your code in the file named ‘question1.m’ (this should be name of your
function too) and resultant image also. Name your output image ‘colorFace.png’.

Problem 02

Now after developing understanding of how the images work and what
different layers represent. We move to more interesting part. In the
assignment folder there is another folder called ‘colorplates’.
There are 4 images inside. One of them is shown in Figure 3. Each image
is concatenation of 3 channels or plates in this case. The photographer
used different filters to generate these 3 separate images, each one
representing one color channel. Hence we will call them “glass plate
image”.
Here channels are, Blue on top then is Green and last one is Red.
NOTE: this part of assignment has been adopted from the A. Efros’s assignment. He is a
faculty member at Berkley.
Question 2a) First task is to read the image and divide the image into 3
separate equal parts such that each part captures separate channel.
Then use them to create a color image. Remember color images we
have been working are RGB where as in the given image they are in BGR
order so be careful when you assign different channels.
Submit a file ‘createColorImage.m’ which should contain function of
same name. The function should input glass plate image and outputs a
color image. Also submit your output on the given images.

Problem 03

Create an image collage of quaid.jpg that is included in the assignment folder.
Image collage is a combination of patches that are stick together to create a
photograph. Figure 5 shows an image collage example, where you can see that
diverse images are put together to generate Obama’s photo.
The assignment folder contains a subfolder “Images”, that contains 4485
images, where each image is of 8x8 size. First, create a new matrix C of same
size as input image to store the collage.
Your task is to iteratively pick a non-overlapping 8x8 patch from input image
using sliding window, and then find the normalized cross correlation of
selected patch with all the images in the “Images” folder. Then place the
image with highest correlation with the patch to matrix C but at the same
pixel coordinates from where that patch was taken (Input Image).
