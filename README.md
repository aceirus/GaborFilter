# Gabor Filter
This is a simple tutorial to explain what the Gabor filter is about and one of it's unique features that made it so popular in practical applications.

I had came across this during one of my projects doing a head pose estimation to provide a human-to-computer (HCI) interface to input commands to play simple online games. This was what made me curious to do my own research in order to gain a better understanding about this.

## Understanding Image Filters
- In the field of image processing, filters play a highly important role.
- All image processing operations can be viewed as applying a series of filters to an image and transforming them to represent it in some way.
- We do this for a varirty of reasons: 
  - understand content of images
  - detect the presence of certain features in the images
  - tranform the images into another domain

## Why do we need this filter?
- For example when you intend to detect edges from an image, these edges might be of any shapes, sizes and orientations.
- When filters are applied to images, we basically modify each pixel in that image and extract some form of information from it.
- Applying this rule globally to an entire image might not be efficient. This is because there are usually not only horizontal edges but also many vertical or even edges that are not sharp.
- To take care of this, the most direct way is to design separate filters that specializes in detecting each of the different cases.
- Natural images usually consist of a large variety of different shapes and sizes, so this is where the Gabor filter was desiged to address this issue.

### 
