# Image-operations
Python image resizing, folder listener.


This program will 'listen' to a folder, files appearing in the folder will be converted to jpg and resized until they are below a specified file size (default 4mb). 

Useful for resizing superresolution images. 

Converted files are moved and archived. 

Uses jpeg quality to resize progressively. *This is not intelligently done and may be slow. 

Could be improved by taking the file size as is and the target then using some formula to set the intial quality value (default 100) much closer to the eventual. 

This is likely only to be of concern on very slow machines or with large numbers of files / high demand. 
