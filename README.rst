Deep Learning Tutorials
=======================

Deep Learning is a new area of Machine Learning research, which has been
introduced with the objective of moving Machine Learning closer to one of its
original goals: Artificial Intelligence.  Deep Learning is about learning
multiple levels of representation and abstraction that help to make sense of
data such as images, sound, and text.  The tutorials presented here will
introduce you to some of the most important deep learning algorithms and will
also show you how to run them using Theano.  Theano is a python library that
makes writing deep learning models easy, and gives the option of training them
on a GPU.

The easiest way to follow the tutorials is to `browse them online
<http://deeplearning.net/tutorial/>`_.

`Main development <http://github.com/lisa-lab/DeepLearningTutorials>`_
of this project.

.. image:: https://secure.travis-ci.org/lisa-lab/DeepLearningTutorials.png
   :target: http://travis-ci.org/lisa-lab/DeepLearningTutorials

Project Layout
--------------

Subdirectories:

- code - Python files corresponding to each tutorial
- data - data and scripts to download data that is used by the tutorials
- doc  - restructured text used by Sphinx to build the tutorial website
- html - built automatically by doc/Makefile, contains tutorial website
- issues_closed - issue tracking
- issues_open - issue tracking
- misc - administrative scripts


Build instructions
------------------

To build the html version of the tutorials, install sphinx and run doc/Makefile

===========================================================================================
@author: lixihua9@126.com
@date:   2015/01/01
@brief:  attensions

1. first run "sh -x download.sh" in data folder in order to download all needed datas.

2. there may be an error with:
"from midi.utils import midiread, midiwrite"
just install midi with:
pip search midi
pip install python-midi

3. run "python test.py" in code folder and see test results.

4. rnnslu failed with no permission to:
http://www-etud.iro.umontreal.ca/~mesnilgr/atis/
http://www-etud.iro.umontreal.ca/~mesnilgr/atis/conlleval.pl
bug fixed:
https://argcv.com/articles/2104.c
http://www.cnts.ua.ac.be/conll2000/chunking/output.html
to get conlleval.txt from web 1 and do "mv conlleval.txt conlleval.pl"
cd /code/rnnslu                 and do "perl conlleval.pl < current.test.txt"
new conlleval.pl may given new index of result:
to change in rnnslu.py(line: 134)

5. lstm failed with pkl file
imdb.pkl fill could be download from:
http://www.iro.umontreal.ca/~lisa/deep/data/imdb.pkl
or add given file path at imdb.py(line: 108) with:
path = "/home/xiaoju/user/lixihua/codingskills/theano/DeepLearningTutorials/data/imdb.pkl.gz"

===========================================================================================
