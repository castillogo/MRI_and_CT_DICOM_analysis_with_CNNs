# MRI_DICOM_analysis_preclinical_models
In this repository you will find a script for analysis of preclinical tumor models with convolutional neural networks and visualization with IPVolume.

This repository needs Tensorflow version 1.14 and pydicom 1.4.2 to properly work.

If you only use small animals scans (which are not too big), you should be able to run everything on your laptop.

Load your MRI DICOM scans into a separate Folder in the main directory of the repository and label the Folder FFE_images.

Save the classifications of the scans into a csv file (here animallist.csv). In this case I only have two classes, since the scans are only of two different tumor models.

run the jupyter notebook final_project_v2.ipynb

In my case, after 15-20 epochs I already got an accuracy on the testing set of 94%.
(letting it run for more epochs might lead to overfitting depending on your dataset).

After running the script final_project_v2.ipynb, a file muchdataXXXXX.npy is created.
(If nothing is changed in the script it should be muchdata-50-50-20.npy)

Use the script 3D_VolumeR1.ipynb to load the .npy file and select the desired scan for visualization with IPVolume (https://github.com/maartenbreddels/ipyvolume).

In theory, this repository should also work for human MRI and CT Data. In this case, you might want to use Amazon AWS for processing. An example of an AWS arquitecture that works can be found in the following slides.

![alt-text](https://github.com/castillogo/MRI_DICOM_analysis_preclinical_models/Folie2.png)

