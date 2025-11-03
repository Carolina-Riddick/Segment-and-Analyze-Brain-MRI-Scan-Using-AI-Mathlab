# <span style="color:rgb(213,80,0)">Segment and Analyze Brain MRI Scan Using AI</span>

This example shows how to preprocess, label, postprocess, and analyze a brain MRI image using MONAI Label.


In this example, you apply the wholeBrainSeg Large UNEST segmentation model \[1\] from the Medical Open Network for AI (MONAI) Label library. The MONAI Label \[2\]\[3\] platform provides fully automated and interactive deep learning models for segmenting radiology images, and you can connect to MONAI Label from within the [Medical Image Labeler](<docid:medical_ref#mw_3fec6056-dc05-42ca-8e06-301307d336b8>) app. To achieve satisfactory results from the wholeBrainSeg Large UNEST segmentation model, you must preprocess your data by registering it to an MNI305 atlas \[4\], which is a standardized brain atlas commonly used in neuroimaging analysis. In this example, you register the brain MRI data to the MNI305 atlas, segment it using the MONAI Label model, and transform the labels back to MRI space to calculate regional brain volumes.

## Import Brain MRI Data

Import the brain MRI scan as a `medicalVolume` object. The MRI volume is from the CANDI data set \[5\] \[6\], and the 2.3 MB scan is attached to this example as a supporting file.
