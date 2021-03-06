Reddit Post Popularity Predictor
====

The "Reddit Post Popularity Predictor" is a online machine learning system that continuously collects new Reddit posts and makes a prediction on their popularity rank after 24 hours. The system is primarily composed of a control unit, which handles the path of execution by delegating tasks to specialized modules. The control unit is multi-threaded, enabling concurrent processing of tasks that have no mutual dependencies. Each specialized module listens over TCP for JSON messages from the control unit. This allows the system to be distributed, which will be greatly beneficial as many resource-intensive computations are carried out. A feedforward neural network is implemented using Keras to predict the popularity of posts. Keywords and phrases are extracted from a Reddit post using RAKE (Rapid Automatic Keyword Extraction). The features used for machine learning are determined using these keywords, as well as karma, post length, account age, etc. After prediction, the control unit will fetch the actual result 24 hours later, using it to train the neural network (stochastic gradient descent).


Dependencies:

Pip to manage python packages:
	sudo port install py27-pip

MySQLdb module for python to connect to MySQL:
	sudo pip install MySQL-python

six module for python for RAKE:
	sudo pip install six

Keras module for Neural Networks:
	sudo pip install keras

Numpy module for Keras:
	sudo pip install numpy

WordNet:
	Princeton University "About WordNet." WordNet. Princeton University. 2010. <http://wordnet.princeton.edu>

RAKE:
	https://github.com/aneesha/RAKE



The source code is released under the MIT License.
