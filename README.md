# Gabor Filter
This is a simple tutorial to explain what the Gabor filter is about and one of it's unique features that made it so popular in practical applications.

I had came across this during one of my projects doing a head pose estimation to provide a human-to-computer (HCI) interface to input commands to play simple online games. This was what made me curious to do my own research in order to gain a better understanding about this.

## Understanding Image Filters
- In the field of image processing, filters play a highly important role.
- All image processing operations can be viewed as applying a series of filters to an image and transforming them to represent it in some way.
- We do this for a variety of reasons: 
  - understand content of images
  - detect the presence of certain features in the images
  - tranform the images into another domain

## Why do we need this filter?
- For example when you intend to detect edges from an image, these edges might be of any shapes, sizes and orientations.
- When filters are applied to images, we basically modify each pixel in that image and extract some form of information from it.
- Applying this rule globally to an entire image might not be efficient. This is because there are usually not only horizontal edges but also many vertical or even edges that are not sharp.
- To take care of this, the most direct way is to design separate filters that specialize in detecting each of the different cases.
- Natural images usually consist of a large variety of different shapes and sizes, so this is where the Gabor filter was desiged to address this issue.

## What is a Gabor filter?
- Gabor filters are orientation-sensitive filters, used for edge and texture analysis.
- It is named after Dennis Gabor, a brilliant Nobel prize winning physicist.
- A Gabor filter can be viewed as a sinusoidal plane of particular frequency and orientation, modulated by a Gaussian wave.

<img src="https://github.com/aceirus/GaborFilter/blob/main/pictures/gabor1.jpg" width=360 height=449 style="float: left; margin-right: 0px;" />

- What this basically means is that a Gabor filter is mathematically structured such that different shapes, sizes, orientations and smoothness can be taken care of.
- A Gabor filter oriented in a particular direction gives a strong response for locations in the target images that have structures in this same orientation.
- To put this in a simple analogy, it is similar to pouring a solidifying liquid onto a mould with unknown structure. Once it solidifies, it will look like the surface of the structure.

## Why is this important?
- Gabor Filters have received considerable attention because of the way it closely resembles the human visual system, such that the characteristics of certain cells in the visual cortex of some mammals can be approximated by these filters.
- Humans have an uncanny ability to process visual data and distinguish things with extreme ease, unlike machines.
- In addition, these filters have demonstrated ability to possess optimal localization properties in both spatial and frequency domains.
- What this means is that Gabor filters will mould itself to suit different scenarios like scale, smoothness and orientation etc. of the edges in a given image.
- Consider an example of an elephant in an image, where it has multiple patterns on its skin in different orientation. In order to highlight all these patterns, we extract these by passing a bank of 16 Gabor filters orientated at 16 different angles.

<img src="https://github.com/aceirus/GaborFilter/blob/main/pictures/gabor16bank.jpg" width=360 height=449 style="float: left; margin-right: 0px;" />

- In the picture below, on the left shows the original input image, while the one on the right shows the patterns on the elephant being highlighted after passing through the Gabor filter bank.
<img src="https://github.com/aceirus/GaborFilter/blob/main/pictures/gabor_elephantDemo.jpg" width=5000 height=450 style="float: left; margin-right: 0px;" />

## Where are they used in practical real life?
The following are useful examples but not limited to:
- Texture segmentation: Separate multiple textures (textons) in an image. This analysis is critical in a lot of areas, including space exploration missions where they have to traverse unknown terrains.
- Optical character recognition (OCR): Automatically recognize handwritten letters and numbers
- Object Recognition: Gabor filters and their modified versions are used extensively in computer vision systems. Since they can closely resemble the human visual system as mentioned above, they are frequently used in designing object recognition systems.
- Edge detection: Detecting edges in an image is a fundamental preprocessing step in many image processing work flows.
- Retina identification: Identifying the retina of humans reliably, which is very important in security systems.
- Image coding: Encoding of images is used almost everywhere for transmission of this information.
