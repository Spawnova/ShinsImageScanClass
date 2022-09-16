# ShinsImageScanClass

ShinsImageScanClass is an AutoHotKey class designed for user freindliness and performance in mind, capable of searching for images and pixels extremely fast and also with background window support it's versatile and lightweight, with no additional dependancies. It also supports 32 and 64 bit.

# Youtube simple overview and examples

[![Video](https://img.youtube.com/vi/wIdcF6KUHIE/default.jpg)](https://www.youtube.com/watch?v=wIdcF6KUHIE)

## Functions
```ruby
#Image....................Find an image; Returns 1 on success and updates returnX and returnY variables; 0 otherwise
Image(image, variance=0, ByRef returnX=0, ByRef returnY=0, centerResults=0, scanDir:=0)

#ImageRegion..............Find an image in a specified region; Returns 1 on success and updates returnX and returnY variables; 0 otherwise
ImageRegion(image, x1, y1, w, h, variance=0, ByRef returnX=0, ByRef returnY=0, centerResults=0, scanDir:=0)

#ImageCount...............Find the amount of images; Returns count of images
ImageCount(image, variance=0)

#ImageCountRegion.........Find the amount of images in a specified region; Returns the count of images inside the region
ImageCountRegion(image, x1, y1, w, h, variance=0)

#ImageClosestToPoint......Finds the closest image to a given position; Returns 1 on success and updates returnX and returnY variables; 0 otherwise
ImageClosestToPoint(image, pointX, pointY, variance=0, byref returnX=0, byref returnY=0, centerResults=0, maxRadius=9999)

#ImageArray...............Finds all images; Returns 1 on success and updates the array variable to contain all image positions; 0 otherwise
ImageArray(image, byref array, variance=0, centerResults=0)

#ImageArrayRegion.........Finds all images in a specified region; Returns 1 on success and updates the array variable to contain all image positions; 0 otherwise
ImageArrayRegion(image, byref array, x1, y1, w, h, variance=0, centerResults=0)

#Pixel....................Find a pixel; Returns 1 on success and updates returnX and returnY variables; 0 otherwise
Pixel(color, variance=0, ByRef returnX=0, ByRef returnY=0, scanDir:=0)

#PixelRegion..............Find a pixel in a specified region; Returns 1 on success and updates returnX and returnY variables; 0 otherwise
PixelRegion(color, x1, y1, w, h, variance=0, byref returnX=0, byref returnY=0, scanDir:=0)

#PixelCount...............Finds the count of pixels; Returns the count of pixels
PixelCount(color, variance=0)

#PixelCountRegion.........Finds the count of pixels in a specified region; Returns the count of pixels in that region
PixelCountRegion(color, x1, y1, w, h, variance=0)

#PixelCountRadius.........Finds the count of pixels in a specified radius; Returns the count of pixels in that radius
PixelCountRadius(color, pointX, pointY, radius, variance=0)

#PixelPosition............Checks a pixel at a specified position; Returns 1 on color match; 0 otherwise
PixelPosition(color, pointX, pointY, variance=0)

#GetPixel.................Gets the pixel at a specified position; Returns pixel color on success; 0 otherwise
GetPixel(x, y)

#SaveImage................Save the current pixel buffer to a png image;
SaveImage(name)

# Image() ImageRegion() Pixel() and PixelRegion() support 8 different scan direction:
# LRTB = Left to Right, from the Top to the Bottom (Default)
# LRBT = Left to Right, from the Bottom to the Top
# RLTB = Right to Left, from the Top to the Bottom
# RLBT = Right to Left, from the Bottom to the Top
# TBLR = Top to Bottom, from the Left to the Right
# TBRL = Top to Bottom, from the Right to the Left
# BTRL = Bottom to Top, from the Right to the Left
# BTLR = Bottom to Top, from the Left to the Right
```

## Notes

* Only for **AHK V1.1**, V2 is not supported!

* When searching for images, using source files without transparency will generally be faster
* Searching for all images such as ImageCount() etc. will take significantly longer when using color variance; when possible try to avoid using color variance if speed is a concern

* I've only tested on my end and can confirm it works for me using 32/64 bit AHK V1.1 on windows 10
* if it doesn't work for you let me know, I may be able to help, or may not just depends.

### Donations

Thanks for stopping by! If you really enjoy my code and want to make a <ins>small</ins> donation, then here's a link! https://www.buymeacoffee.com/Spawnova

**I will continue to provide code, and support released classes regardless of any monetary support**, and I'd rather none is given if you are not comfortably in a position to do so!
