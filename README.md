# Open Source Library of Pelvis Segmentation and Planning Atlas

It is difficult to find pelvis atlas in the public domain for image segmentation, surface modeling via Active Shape Model, and surgical trajectory planning. To address this issue, this open-source library of pelvis atlas is constructed to provide pelvis CT images, segmentations, statistical shape models and percutaneous screw trajectories. The library is freely available for academic or educational use. 

The library was developed at I-STAR Lab at Johns Hopkins University.

# User Instructions

The atlas library contains 5 folders: image, segmentation, surface, SSM and trajectory.

**Image:** The image folder contains 40 CT images of the pelvis modified from The Cancer Imaging Archive (TCIA) CT Lymph Node database. For the original CT images, please go to the original database: https://wiki.cancerimagingarchive.net/display/Public/CT+Lymph+Nodes.  

**Segmentation:** The segmentation folder contains indivisual segmentations of left hip, right hip and sacrum (S1-S3) correponding to each CT image. Segmentations are saved in surface .stl format.

**Surface:** The surface folder contains post-processed left hip, right hip and sacrum (S1-S3) surfaces in .stl format. Each surface is remeshed into triangulated mesh with 5000 vertices. Surfaces of each bone have corresponding vertices.

**SSM:** The SSM folder contains the statistical shape model of the individual left hip, right hip and sacrum (S1-S3) in .h5 format. Please refer to our journal paper [1] for details.

**Trajectory:** The trajectory folder contains annotated volumetric trajectory surfaces for each pelvis in .stl format. 10 different trajectory types are included: AIIS Left / Right, Iliac Crest Left / Right, Posterior column Left / Right,Superior Ramus Left / Right, Iliosacral S1 and Iliosacral S2. Each trajectory file is a triangulated surface mesh with 500 vertices that contains most possible trajectories in the corresponding bone corridor.

# Citation

**For use of this open-source library, please cite the following paper:**
R. Han, A. Uneri, T. De Silva, J. Goerres, M. Ketcha, B. Ramsay, S. Vogt, G. Kleinszig, G. Osgood, J. H. Siewerdsen, Automatic Planning and Fluoroscopic Guidance in Pelvic Trauma Surgery Using Atlas-Based Registration. XXXXXXXXXXXXXXX

**Please also cite the following for the TCIA Lymph Node CT image files:**
Holger, Roth, Lu, Le, Seff, Ari, Cherry, Kevin M, Hoffman, Joanne, Wang, Shijun, … Summers, Ronald M. (2015). A new 2.5 D representation for lymph node detection in CT. The Cancer Imaging Archive. http://doi.org/10.7937/K9/TCIA.2015.AQIIDCNM

Roth, Holger R and Lu, Le and Seff, Ari and Cherry, Kevin M and Hoffman, Joanne and Wang, Shijun and Liu, Jiamin and Turkbey, Evrim and Summers, Ronald M. A new 2.5 D representation for lymph node detection using random sets of deep convolutional neural network observations. Medical Image Computing and Computer-Assisted Intervention--MICCAI 2014, p520-527, 2014. (link)

Seff, Ari and Lu, Le and Cherry, Kevin M and Roth, Holger R and Liu, Jiamin and Wang, Shijun and Hoffman, Joanne and Turkbey, Evrim B and Summers, Ronald M. 2D view aggregation for lymph node detection using a shallow hierarchy of linear classifiers. Medical Image Computing and Computer-Assisted Intervention--MICCAI 2014, p544-552, 2014. (link)

**And cite the TCIA database publication**
Clark K, Vendt B, Smith K, Freymann J, Kirby J, Koppel P, Moore S, Phillips S, Maffitt D, Pringle M, Tarbox L, Prior F. The Cancer Imaging Archive (TCIA): Maintaining and Operating a Public Information Repository, Journal of Digital Imaging, Volume 26, Number 6, December, 2013, pp 1045-1057. (paper)
