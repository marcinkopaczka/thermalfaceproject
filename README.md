# thermalfaceproject
Thermal face detection, tracking and analysis

This is the repository for the paper "A fully annotated thermal face database and its application for thermal facial expression recognition", published at IEEE I2MTC 2018

https://ieeexplore.ieee.org/document/8409768/

direct PDF link (free):
http://www.lfb.rwth-aachen.de/wp-content/plugins/bibtex/show_pdf.php?file=KCZ18d.pdf

The repository is currently being prepared and set up. below you will find some preliminary usage instructions for a quick start. If you're interested in the the database itself for research purposes, please contact me directly at 

marcin.kopaczka@lfb.rwth-aachen.de

As soon as we find a good solution to host the database we will provide a link here.


=====Preliminary version. Is currently updated frequently, consider this file work-in-progress.=====

1 Using the database

1.1. basic usage instructions

The simple version of the database is enough for most projects. It contains the database images in PNG format and the landmarks in LJSON and PTS format.

You can use the database in any programming language and programming setup you want to. The .pts files in the database are a plain text format containing the landmark coordinates, any programming language should be able to read them as well as the .png files. We will upload Code snippets in MATLAB and C++/OpenCV that show how the data can be loaded. We used the database for projects in these languages and they work perfectly fine. Java and other high-level languages should work equally well. That's for those that need to stick to existing code or have other requirements towards the used programming environment.

However, if possible, we strongly suggest that you use Python together with the powerful Menpo library. With few exceptions, all algorithms described in our papers are available in Python and most of our own codebase is written in it. Most of the code covered in the documentation will refer to Python/Menpo as well. So if you're just getting your research started or need to get results quickly without diving too deep into code (for example because you are not developing any algorithms for face tracking but need some face or landmark detection running ASAP for your project) then follow these instructions to get a working environment for our database running.

* Get Miniconda and Menpo. There are excelent instructions on the Menpo homepage, follow these:
http://www.menpo.org/installation/conda.html
(we will update this page soon with full install instructions, until then sitck to the Menpo install guide)

Get Miniconda in Python 3.6 (or newer if available) in 64 bit.

When following the environment setup, use the following linse for environment creation instead of the one given in the installation instruction. This will get you a Python 3.5 environment; most of our code is in 3.5 for compatibiliy reasons with other libraries that we use (you MAY get everything running with the newest versions, but we won't be able to give any help if you use a different environment than we do):

conda create -n thermalfaceproject python=3.5
activate thermalfaceproject
conda install -c menpo menpoproject menpo=0.7.7
conda install skimage

sometimes, skimage installation fails from Conda, get it from PIP then with pip install skimage.

We strongly recommend you spend some time with Menpo as it offers a large number of excellent algorithms for face and landmark detection. Check out the menpo notebooks from github; make sure you get the notebooks for your menpo and menpofit version.

NOTE: training the algorithms from scratch may need some time (basic face detectors and AAMs need like an hour on the database; some methods such as a VJ-detector or the DAN need days and may require a good GPU). You will need a decent machine; training a full feature-based AAM needs at least 64 GB of RAM, potentially more. We will provide pre-trained detectors as pickle files in the near future. These will be able to un on less powerful PCs.

Once you have your database from us and your environment running, the fun starts:

1.2 face detection
1.3 facial landmafk detection and face tracking

(uploading notebook in a few days)
