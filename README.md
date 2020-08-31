# Face-Recognition

Neural Network implementation that tries to classify face on an image, more specifically, it tries to detect 19 points on the face:  

<ul> 
<li>left eye center x and y</li>
<li>right eye center x and y</li>

<li>left eye inner corner x and y</li>
<li>right eye inner corner x and y</li>

<li>left eye outer corner x and y</li>
<li>right eye outer corner x and y</li>

<li>left eyebrow inner end x and y</li>
<li>right eyebrow inner end x and y</li>

<li>left eyebrow outer end x and y</li>
<li>right eyebrow outer end x and y</li>

<li>left eyebrow inner end x and y</li>
<li>right eyebrow inner end x and y</li>

<li>left eyebrow outer end x and y</li>
<li>right eyebrow outer end x and y</li>

<li>nose tip x and y</li>

<li>mouth left corner x and y</li>

<li>mouth right corner x and y</li>

<li>mouth center top lip x and y</li>

<li>mouth center bottom lip x and y</li>
</ul>


## Dealing with missing data

Many of these points were None values, so i decided to remove them from the dataset (in this version of application), because face points are very precise and the type of supervised learning here was regression, so i didn't want to
aggregate anything.

When data is removed, we get 15 points. on the face, that need to be "classified" on test images.

## Network architecture
For this task, i decided to use:
<ul>
<li>6 convolution layers, where only first two had MaxPooling implemented(to speed up the training and save memory)</li>
<li>4 fully connected layers</li>
</ul>

Detailes about the network can be found in *Face_Recognition.ipynb*

## Results
![titanic_image](https://i.postimg.cc/xCTWhkff/test-image.png)