# Open Source Atlas of Pelvis Segmentations and Surgical Trajectories


This open-source pelvis atlas is constructed to provide pelvis CT segmentations, statistical shape models, and surgical screw trajectories.
The atlas is freely available for academic or educational use. 
For research only.

The atlas was developed at I-STAR Lab at Johns Hopkins University.
Contact Jeff Siewerdsen (jeff.siewerdsen@jhu.edu ) with questions. This atlas can also be downloaded from https://istar.jhu.edu/downloads/

The atlas was first published in the following journal publication.
Please cite the following:
[1] Han R, Uneri A, Silva T D, Ketcha M, Goerres J, Vogt S, Kleinszig G, Osgood G, Siewerdsen J H, Atlas-Based Automatic Planning and 3D-2D Fluoroscopic Guidance in Pelvic Trauma Surgery. Phys. Med. Biol. https://doi.org/10.1088/1361-6560/ab1456

# Contents
The atlas contains 4 folders:
/segmentation/
/surface/
/SSM/
/trajectory/
/table.csv

**Image:** 
The atlas derives from 40 CT images of the pelvis adapted from The Cancer Imaging Archive (TCIA) CT Lymph Node database. 
For the original CT images, please go to the original database:
https://wiki.cancerimagingarchive.net/display/Public/CT+Lymph+Nodes  

A table relating the 40 atlas members to specific CT images in the TCIA database can be found here:
/table.csv

**Segmentation:** 
The segmentation folder contains individual segmentations of left hip, right hip, and sacrum (S1-S3) correponding to each CT image.
Segmentations are in *.stl format.

**Surface:** 
The surface folder contains surfaces of left hip, right hip, and sacrum (S1-S3) in *.vtk format.
Each surface is remeshed into a equidistant triangulated mesh with 5000 vertices.
Vertices are ordered in each bone surface to provide correspondence between each atlas member.
.vtk format maintains vertices order, whereas .stl format does not.

**SSM:** 
The SSM folder contains the statistical shape model of the individual left hip, right hip, and sacrum (S1-S3) in .h5 format.
The file is structured as:
 ./model/mean (SSM mean)
 ./model/pcaBasis (principal coefficient matrix)
 ./model/pcaVariance (principal component variances)
 ./representer/cells (surface face matrix 3*Nf (# of faces))
 ./representer/points (surface vertices matrix 3*Nv (# of vertices))
 Please refer to our journal paper [1] for details.

**Trajectory:** 
The trajectory folder contains annotated volumetric trajectory surfaces for each pelvis in .stl format. 
10 trajectory types are included: 
/AIIS_Left/
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/ Right
Iliac Crest Left / 
Right
Posterior column Left / 
Right
Superior Ramus Left / 
Right
Iliosacral S1 
Iliosacral S2.
Each trajectory file is a triangulated surface mesh with 500 vertices in a particular bone corridor.

# References

**For use of this open-source library, please cite the following paper:**
[1] Han R, Uneri A, Silva T D, Ketcha M, Goerres J, Vogt S, Kleinszig G, Osgood G, Siewerdsen J H, Atlas-Based Automatic Planning and 3D-2D Fluoroscopic Guidance in Pelvic Trauma Surgery. Phys. Med. Biol. https://doi.org/10.1088/1361-6560/ab1456

**Please also cite the following for the TCIA Lymph Node CT image files:**
[2] Roth H, Le L, Seff A, Cherry K, Hoffman J, Wang S, Summers R. (2015). A new 2.5 D representation for lymph node detection in CT. The Cancer Imaging Archive. http://doi.org/10.7937/K9/TCIA.2015.AQIIDCNM

[3] Roth H, Lu L, Seff A, Cherry K, Hoffman J, Wang S, Liu J, Turkbey E, Summers R. A new 2.5 D representation for lymph node detection using random sets of deep convolutional neural network observations. Medical Image Computing and Computer-Assisted Intervention--MICCAI 2014, p520-527, 2014. 10.1007/978-3-319-10404-1_65

[4] Seff A, Lu L, Cherry K, Roth H, Liu J, Wang S, Hoffman J, Turkbey E, Summers R. 2D view aggregation for lymph node detection using a shallow hierarchy of linear classifiers. Medical Image Computing and Computer-Assisted Intervention--MICCAI 2014, p544-552, 2014. 

**And cite the TCIA database publication**
[5] Clark K, Vendt B, Smith K, Freymann J, Kirby J, Koppel P, Moore S, Phillips S, Maffitt D, Pringle M, Tarbox L, Prior F. The Cancer Imaging Archive (TCIA): Maintaining and Operating a Public Information Repository, Journal of Digital Imaging, Volume 26, Number 6, December, 2013, pp 1045-1057. (paper)
