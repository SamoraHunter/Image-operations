###### Image-operations

## Python image resizing, folder listener.

  This program will 'listen' to a folder, files appearing in the folder will be converted to jpg and resized until they are below a specified file size (default 4mb). 

  Useful for resizing superresolution images. 

  Converted files are moved and archived. 

  Uses jpeg quality to resize progressively. *This is not intelligently done and may be slow. 

  Could be improved by taking the file size as is and the target then using some formula to set the intial quality value (default 100) much closer to the eventual. 

  This is likely only to be of concern on very slow machines or with large numbers of files / high demand. 
  
# Image similarity check, opencv, numpy, multiprocessing
set the path to the archive will all the images to be compared, each image will be compared to each other image in the archive.
images must be the same dimension
set the threshold for comparison below, the closer to zero the more similar images must be to warrant archiving
Intended usage: run the script with a folder of images set, the script will leave only non similar images in the archive
Set the number of logical cores you have. I have a 12 core with 24 logical so I set 24.

Example: You have a large number of images, some are almost duplicates for example taken only a frame apart. An image hash comparison would fail to sort them here. 
Supply a folder containing the images, and I suggest playing with the threshold calling just the 'mse' function on two images you would like the script to differentiate to get a good threshold value. 
