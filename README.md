# MeanShapeJ

## Introduction
In biomedical image analysis, many tasks rely on an underlying image segmentation step which affects often greatly further downstream analysis. Therefore, both improving and knowing the accuracy of the segmentation is necessary to be able to assess the analysis accuracy itself. The former can be established by segmenting the same images by multiple expert annotators and fusing the resulting labels or masks to a single segmentation, while the accuracy can then be measured by looking at the agreement between the annotators. Popular techniques such as STAPLE consider each pixel separately, thereby allowing very complex but also often unrealistic complex resulting estimations for best fused labels. Here we introduce a contour-averaging technique which obtains a ground truth estimation as a smooth curve from multiple region annotations and retains their local features. The metric defined by the approach can be both used to give outliers less weight in the average curve as well as to estimate the accuracy of the final segmentation. By virtue of the method, it is also applicable for obtaining smooth transitions between two different segmentations. The proposed algorithm is based on a contour energy minimization by a variational method.

We have implemented it both as a ImageJ plugin (this repo), a C++ version, Python script (MeanShapePy), and a MATLAB script (MeanShapeM). This version is specifically made to allow batch calculations while the other implementations are more oriented to test the working of the algorithm, and give the opportunity to the developpers to pick their own language of choice.

## Getting started

MeanShapeJ is is a FIJI (ImageJ) plugin. Fiji can be downloaded from www.fiji.sc.

An example dataset with downscaled brain slices and brain region annotations can be found in the dataset subfolder [still have to upload the example set]

To install the MeanShapeJ plugin copy the jar-file MeanShapeJ_-1.0-SNAPSHOT.jar into the plugins folder and unzip the file MeanShapeLibs.zip (the necessary dependencies not included in FIJI) into the jars folder of the ImageJ/FIJI application (typically this folder is …/Fiji.app/jars/). This second method avoids possible collisions between existing libraries in FIJI and MeanShapeJ's dependencies.

The plugin can then be called from Plugins > MeanShapeJ > MeanShapeJ. 

To use MeanShapeJ directly one can also just start it (by e.g. double clicking it, this works only for the MeanShapeJ_-1.0-SNAPSHOT-jar-with-dependencies.jar file), this way it will open its own ImageJ instance to run in.

Further explaination of the usage and input/output of the MeanShapeJ plugin is given in the *user_manual.pdf* file. [still have to generate the manual]

## Authors

Jozsef Molnar, Michael Barbier, Winnok De Vos, and Peter Horvath
