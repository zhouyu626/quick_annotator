# QuickAnnotator

[//]: # (add some description here)

### User Manual
##### 1. Update Chrome to latest version
##### 2. Open terminal, start the server
```
cd quick_annotator
python3.6 QA.py
``` 
##### 3. Open Chrome, go to
```
http://129.22.136.73:5555
```

##### 4. Create a new project, add images to the project
<div align="center">
    <img src="https://github.com/zhouyu626/quick_annotator/blob/master/Images/Step1_CreateProject.gif"/>
</div>

##### 5. Open an image, press and hold the left mouse button down and move the mouse to the desired position to crop a patch from the image. The cropped region will display in the annotator in the bottom left. Use the "Crop Size" slider to change the cropping size.
<div align="center">
    <img src="https://github.com/zhouyu626/quick_annotator/blob/master/Images/Step2_ChooseCroppingSize.gif"/>
</div>

##### 6. The annotator toolbox includes (from left to right, top to bottom):
##### (1) Freehand (2) Magic wand (3) Intelligent scissor (4) Paint the region annotated by intelligent scissor (5) Eraser (6) Remove object (7) Reset canvas (8) Annotate positive region (9) Paint all the un-annotated regions to negative (10) Annotate unknown region (11) Undo (12) Redo (13) Add current sample to training set (14) Add current sample to testing set

##### 7. To use the freehand tool, press and hold the left mouse button down and move to make quick, free-form shapes.
<div align="center">
    <img src="https://github.com/zhouyu626/quick_annotator/blob/master/Images/Step3_Annotate_freehand.gif"/>
</div>

##### 8. To use the magic wand tool, press and move the left mouse button to select areas of similar color. Change the tolerance slider to adjust the sensitivity of the magic wand selection. 
<div align="center">
    <img src="https://github.com/zhouyu626/quick_annotator/blob/master/Images/Step3_Annotate_MagicWand.gif"/>
</div>

##### 9. To use the intelligent scissor tool, click on the first desired point and wait for about 3 seconds until a curve connecting your current mouse location with the first point is shown in the image. The curve will try to follow edges in the image and connect your mouse location with the last point all the time. You can adjust the curve by moving the mouse and once you are satisfied, click on the right location to add a new point and wait for about 2 seconds to start choosing the next point. The selection is closed when you are clicking the last point over the first one and then clicking the X button in the toolbox (the 4th button in the 1st row).
<div align="center">
    <img src="https://github.com/zhouyu626/quick_annotator/blob/master/Images/Step3_Annotate_IntelligentScissors.gif"/>
</div>

##### 10. When using the intelligent scissor, you can right click anywhere inside the image to remove the last point and go one step back.
<div align="center">
    <img src="https://github.com/zhouyu626/quick_annotator/blob/master/Images/Step3_Annotate_IntelligentScissors_Undo.gif"/>
</div>

##### 11. Use eraser, remove object and reset canvas tools to modify or clear the annotation. Use undo and redo to cancel or redo your last action.
<div align="center">
    <img src="https://github.com/zhouyu626/quick_annotator/blob/master/Images/Step3_Annotate_Eraser_Remove_ClearCanvas_Redo_Undo.gif"/>
</div>

##### 12. When finish annotating the cropped patch, click on the "N" button to fill all the un-annotated area with negative. Click the "Tr" button to add the current annotated patch to training set. 
<div align="center">
    <img src="https://github.com/zhouyu626/quick_annotator/blob/master/Images/Step5_AddTrainingSample.gif"/>
</div>

##### 13. Click the "Te" button to add the current annotated patch to testing set. Note that at least one testing sample should be added before training a deep learning model. 
<div align="center">
    <img src="https://github.com/zhouyu626/quick_annotator/blob/master/Images/Step4_AddTestingSample.gif"/>
</div>

##### 14. Deep learning model will be trained after certain amount of training and testing samples are added to the dataset. The first triggering condition is (testing = 1, training = 3). Refresh the webpage to view deep learning output. You can click on the "Train a new model" and "Generate DL output" in the top menu bar to manually train a new model or generate deep learning output.
<div align="center">
    <img src="https://github.com/zhouyu626/quick_annotator/blob/master/Images/Step6_GenerateDLModel.PNG"/>
</div>

##### 15. Click the buttons under the "View" drop-down menu or use hot keys A/S/D/F to change display content. 
<div align="center">
    <img src="https://github.com/zhouyu626/quick_annotator/blob/master/Images/Step7_ViewDLResult.gif"/>
</div>

##### 16. Select a patch from the image and modify the deep learning output to add new annotation samples to the training set. By default the annotator displays a fused image of dl result and annotation, click View->DL Result (Annotator) or press G key to display only the deep learning output. 
<div align="center">
    <img src="https://github.com/zhouyu626/quick_annotator/blob/master/Images/Step8_ModifyDLResult.gif"/>
</div>

##### 17. Repeat 14-16.

##### 18. Download DL model, output or annotation files by clicking Download->Model/DL result/Annotation button in the top menu bar.
