Lens Blur
=========

Lens Blur is an example application for Windows Phone demonstrating the use of two new Imaging SDK APIs, Interactive Foreground Segmenter and Lens Blur Effect. Interactive Foreground Segmenter is first used to create a mask (foreground/background), after which Lens Blur Effect (aka “bokeh”) is applied to the areas that were marked as background.

This example application is hosted in GitHub:
https://github.com/microsoft/lens-blur/

For more information on implementation visit Lumia Developer's Library: http://go.microsoft.com/fwlink/?LinkId=528375

Developed with Microsoft Visual Studio Express 2012 for Windows Phone.

Compatible with:

 * Windows Phone 8

Tested to work on:

 * Nokia Lumia 520
 * Nokia Lumia 1020
 * Nokia Lumia 1520


Instructions
------------

Make sure you have the following installed:

 * Windows 8
 * Visual Studio Express 2012 for Windows Phone
 * Nuget 2.7 or later

To build and run the sample in emulator

1. Open the SLN file:
   File > Open Project, select the solution (.sln postfix) file
2. Select the target 'Emulator' and platform 'x86'.
3. Press F5 to build the project and run it.


If the project does not compile on the first attempt it's possible that you
did not have the required packages yet. With Nuget 2.7 or later the missing
packages are fetched automatically when build process is invoked, so try
building again. If some packages cannot be found there should be an
error stating this in the Output panel in Visual Studio Express.

For more information on deploying and testing applications see:
http://msdn.microsoft.com/library/windowsphone/develop/ff402565(v=vs.105).aspx


About the implementation
------------------------

| Folder | Description |
| ------ | ----------- |
| / | Contains the project file, the license information and this file (README.md) |
| LensBlurApp | Root folder for the implementation files.  |
| LensBlurApp/Assets | Graphic assets like icons and tiles. |
| LensBlurApp/Models | Application models. |
| LensBlurApp/Pages | Application pages. |
| LensBlurApp/Resources | Localized resources. |
| LensBlurApp/Properties | Application property files. |

Important classes:

| Class | Description |
| ----- | ----------- |
| Pages.EffectPage | Contains code for applying the blur effect. |
| Pages.SegmenterPage | Contains code for the foreground/background segmentation. |


Known issues
------------

 * Application tombstoning is not supported.
 * Saving high resolution photos may run out of memory on low-memory devices.


License
-------

See the license text file delivered with this project:
https://github.com/microsoft/lens-blur/blob/master/License.txt

See the attributions text file for a list of built-in gallery photo attributions:
https://github.com/microsoft/lens-blur/blob/master/Attributions.txt

Version history
---------------

 * 1.1.0.0: Second public release of Lens Blur
   - Built-in photo gallery to easily start testing the segmenter and the lens blur effect
   - Moved reset (annotations) button to menu
   - Effect settings are now preserved between effect configuration sessions
   - Updated blur kernel shape selection button icons to match the actual shapes
   - Photo zooming: on effect page you can now tap on the photo to enter a fullscreen zoom view
   - Changed application icon and tiles to Nokia Developer style

 * 1.0.0.0: First public release of Lens Blur
