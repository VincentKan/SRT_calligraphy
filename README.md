# SRT_calligraphy
SRT project of evaluating and optimizing Chinese characters calligraphy. 
This project includes loading the character as monochronic graph to 0-1 matrix and refine it to get better pattern.
Futhermore, we feed these patterns to CNN to get the best range (interval) of these parameters.
---

## Code Illustration

* general.py
* imgproc.py
* carwler/catch.py
* list_proc.py

---
### general.py</br>
---
Argument Storation</br>
incomplete
---
Name|Meaning
------|------
two_threshold|Threshold for transforming a RGB picture into a black-white picture
---

### imgproc.py</br>
---
Picture Basic Produce</br>
complete
---
Function|Argument|Illustration
--------|---------|--------
imgread|file address|read pictrue(jpg), and transform it into a matrix(2d)
imgshow|picture matrtix|show picture, press any key to quit
matread|pictrue matrix|return a num matrix construct by 0 and 1, 0 mean white,1 mean black
matwrite|number matrix|return a pictrue matrix
matget|file address|read pictrue, and return a num matrix directly
pos_black|number matrix|get all black pot, and return a list with all postion[x,y] of black point
convexhull|picture or number matrix|return the turning point of the convex hull
drawconvex|picture matrix,contours|draw convex into pictrue matrix
findcenter|matrix, isimg(bool)=False|when isimg is False,this function accept num matrix(0,1),yet it accept image matrix(0,255)
findaxis|number matrix|return the axis of the black point calculated by linear regression
matclear|number matrix|clear up the little point in a matrix 