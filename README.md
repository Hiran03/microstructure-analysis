# Detection of M-A Islands in Bainite Micrographs Using Convolutional Neural Networks

Microstructure analysis of welds and other steels has always been time-consuming and labor-intensive. The
weld must have good physical properties and specic composition, but these tend to be inconsistent. There is a
demand in the industry to automate it as much as possible, speeding up this process many times. We tried to
address this problem via a Machine learning based approach. For this purpose, we attempted to solve a very
special case of segmenting Martensite-Austenite (MA) islands on bainitic steels using a Mask Region-based
convolutional neural network (Mask-R CNN).

Classifying dierent morphological features would require dierent ML treatment. So we categorized the microstructure into following categories.
Class 1- Elongated islands (Regime I and IV)
Class 3- Blocky islands (Regime III)
Class 2 -Mixed of bothe (Regime II)

Now that with that domain knowledge acquired the problem can be split into smaller sub-problems:
1. Detecting instances (MA- islands) and forming a bounding box. (was done using an unsupervised learning technique, K-Means)
2. Classication of the instance into one of the two morphologies blocky and elongated. (was done using a CNN framework)
3. Training separate Mask R-CNN models for each class.

![image](https://github.com/user-attachments/assets/ba1c0693-9dc2-400f-b1d9-b20bbc0fc318)

**Files**

Dataset : https://figshare.com/articles/dataset/Image_data_and_labels/19232523 

1. report.pdf - Detailed report of the project.
2. Datsetgen.py - Read dataset for K-Means
3. KMeans.ipynb - impementing K_means for island detection.
4. cnn(1).ipynb - Classification of the detected island (blocky - elongated)
5. Detectron2.ipynb - Mask R-CNN for segmentation
6. Data_augmentation.ipynb - Auxilary program do generate augmentated data.


