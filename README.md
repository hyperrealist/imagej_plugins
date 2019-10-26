# iterativePIV
This is a mirror of the PIV (Particle Image Velocimetry) ImageJ plugin [iterativePIV](https://sites.google.com/site/qingzongtseng/piv) ([and other](https://sites.google.com/site/qingzongtseng/imagejplugins)) [ImageJ](http://imagej.nih.gov/ij/) plugins by Qingzong TSENG as retrieved on 26 October 2019.

## Description

This [ImageJ](http://imagej.nih.gov/ij/) plugin performs iterative particle image velocimetry (PIV) analysis. Basically, a pair of images is divided into smaller regions (interrogation windows). The cross-correlation between these image subregions measures the optic flow (displacement or velocity of the objects) within the image pair. By progressively decreasing the interrogation window size, a better PIV resolution can be achieved. 

Two image correlation methods were implemented for the optic flow measurement. One can either use the conventional cross-correlation method, which compares two interrogation windows with the same size; or one can use the template matching method with normalized correlation coefficient algorithm, where the interrogation window is compared against a larger searching window. 

The result of the PIV analysis will be displayed as a vectorial plot, and saved in plain text tabular format containing all the analysis result. This plugin also provide a plot function to visualize the vectorial data with selected color coding. 

This plugin was originally developed for measuring the displacement field of Traction Force Microscopy (TFM). It might be somehow rudimentary compared with other specialized PIV program (such as [JPIV](http://www.jpiv.vennemann-online.de/), [mpiv](http://www.oceanwave.jp/softwares/mpiv/index.php), [openPIV](http://www.openpiv.net/)....etc.). Nevertheless, the implementation as ImageJ plugin makes it more available to general public and easier to combine with other image processing tasks. Compared with the plugin PIV analyser, this plugin provides more flexibility in terms of multiple PIV iteration, different correlation algorithm, as well as data retrieval and processing. 

## Downloads
You can download this iterativePIV plugin [PIV_.jar](https://github.com/hyperrealist/imagej_plugins/blob/master/legacy/PIV_.jar)
System independent javacv library files: [javacv.jar](https://github.com/hyperrealist/imagej_plugins/blob/master/legacy/libs_javacv0.1_opencv2.4/javacv.jar), [javacpp.jar](https://github.com/hyperrealist/imagej_plugins/blob/master/legacy/libs_javacv0.1_opencv2.4/javacpp.jar) , [opencv.jar](https://github.com/hyperrealist/imagej_plugins/blob/master/legacy/libs_javacv0.1_opencv2.4/opencv.jar)
System-dependent library files: [32-bit Windows](https://github.com/hyperrealist/imagej_plugins/blob/master/legacy/libs_javacv0.1_opencv2.4/opencv-windows-x86.jar) , [64-bit Windows](https://github.com/hyperrealist/imagej_plugins/blob/master/legacy/libs_javacv0.1_opencv2.4/opencv-windows-x86_64.jar), [64-bit Mac](https://github.com/hyperrealist/imagej_plugins/blob/master/legacy/libs_javacv0.1_opencv2.4/opencv-macosx-x86_64.jar), [32-bit Linux](https://github.com/hyperrealist/imagej_plugins/blob/master/legacy/libs_javacv0.1_opencv2.4/opencv-linux-x86.jar) or [64-bit Linux](https://github.com/hyperrealist/imagej_plugins/blob/master/legacy/libs_javacv0.1_opencv2.4/opencv-linux-x86_64.jar) are also required for full functionality.

#### For ImageJ running on Java 1.8, or having any javacv library compatibility issues, please download the updated plugin file and library files at [this](https://github.com/qztseng/imagej_plugins/tree/master/current) github repository instead.

### Important:
If you want to do PIV with different interrogation and search window size, which is more robust, you will need the OpenCV / javacv library files.
Please see Installation for more details. 
Otherwise, only use the "PIV>iterative PIV(Cross-correlation)..." function.

## System Requirements
ImageJ 1.48 or later, running on Java 1.6
For ImageJ running on Java 1.8, please download the updated plugin file and library files at [this](https://github.com/qztseng/imagej_plugins/tree/master/current) github repository.

## Installation
Just put the downloaded PIV_.jar to your ImageJ plugins folder, and restart ImageJ. You will find this plugin under the ImageJ menu Plugins>PIV. 

However, if you want to do  PIV with the template matching method (window size unlimited by the power of 2, and interrogation window compared with a larger searching window), you will also need the OpenCV / javacv library files. Put the system-independent javacv library files: javacv.jar, javacpp.jar , opencv.jar into your ImageJ's plugins folder.
Depending on your system architecture, put one of the following files: 32-bit Windows , 64-bit Windows, 64-bit Mac, 32-bit Linux or 64-bit Linux into your ImageJ's plugins folder.
