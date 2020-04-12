# Workbench for exporting a FreeCAD model to POV-Ray

**With this workbench you will be able to create easily photorealistic pictures of your model, even if you're a beginner in raytracing. If you're an advanced users with more knowledge, you can get the full control about all detailed settings.**

![Logo and Renderings](README_img.png)

The export macro is intended to export the FreeCAD model structure with their equivalent in POV-Ray.
In contrast to other solutions for exporting FreeCAD models to POV-Ray, this macro tries to make the file clearly and easy to edit. For that, it doesn't create gigantic meshes, it moves the tree structure with the boolean operations into a POV-Ray file.  
Until now, the macro supports most objects from the Part Workbench and some features from the Part design and Draft workbench. Not supported objects are simulated with meshes (see [Supported Objects](#supportedObjects)).

To give the user the full control, you can define extra things or another surface as in FreeCAD (Please visit the [Wiki](doc/index.md) for more information).

## Installation
**Automatic Installation**  
The recommended way of installing this workbench is to use the addon manager (Tools / Addon Manager). In the addon manager in the workbenches tab, select the XXX-Workbench and click install.

**Manual Installation**  
Download the repository from [gitlab.com/usbhub/exporttopovray](https://www.gitlab.com/usbhub/exporttopovray) XXX and unpack the zip in ~/.FreeCAD/Mod.

## Features
* easy applying of textures
* easy use of indirect lightning to create realistic images
* easy inserting and configuration of different types of lights  
  **⇨ simple handling and operation**
* power users can get the full control about the whole configuration with the user inc file (see [Power Users](doc/powerusers.md))  
  **⇨offering all settings for advanced users**
* the model is not converted into meshes, the model will be converted into a mathematical way of describing the object shape, so you will get a better object and a better picture
* very good readability of the created files → easy editing of these files

## Advantages compared with the Raytracing Workbench
* You can use **all** POV-Ray features
* Easy changing of materials / textures of objects
  - To change the material of an object in the Raytracing Workbench, you have to know a lot about POV-Ray and write the changes manually to the created pov file. If you change you model and render again, you have to do all changes again.
  - With the macro, you can easily choose a material in the textures tab and the changes will be saved (and you don't need any POV-Ray knowledge)
* The macro is easier to use
* The macro uses a right handed coordinate system like FreeCAD
* WYSIWYG
* The macro is written in Python, so it is easier for extending
* The macro takes more object properties than the workbench
* The macro reproduces the tree structure and doesn't create gigantic meshs
  * → Better understanding & editing of the file
  * → Better performance
  * → Better renderings
