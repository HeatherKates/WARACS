# WARACS
WARACS: Wrappers to Automate the Reconstruction of Ancestral Character States

### - Prerequisites
* Python v.2.7 (https://www.python.org/download/releases/2.7/)
* Python package *setuptools* (https://pypi.python.org/pypi/setuptools)

### - Wrapped Applications
* Mesquite (http://mesquiteproject.org)
* BayesTraits (http://www.evolution.reading.ac.uk/BayesTraits.html)
* TreeGraph2 (http://treegraph.bioinfweb.info/)

### - Python Dependencies
* Python package *DendroPy* (https://pypi.python.org/pypi/DendroPy)
* Python package *numpy* (https://pypi.python.org/pypi/numpy)
* Python package *PrettyTable* (https://pypi.python.org/pypi/PrettyTable)

### - Basic Usage
###### 1. Test the wrapper
```
python2.7 /path_to_git/WARACS/WARACS_Mesquite.py -h
```
###### 2. Perform an ancestral character state reconstruction via [Mesquite](http://mesquiteproject.org)
```
python2.7 /path_to_git/WARACS/WARACS_Mesquite.py
  -c /path_to_input/character_state_distribution.csv
  -t /path_to_input/tree_distribution.tre
  -p /path_to_input/plotting_tree.tre
  -o likelihood
  -n 2
  -s /path_to_Mesquite/mesquite.sh
  -v True
```
###### 3. Perform an ancestral character state reconstruction via [BayesTraits](http://www.evolution.reading.ac.uk/BayesTraits.html)
```
python2.7 /path_to_git/WARACS/WARACS_BayesTraits.py
  -c /path_to_input/character_state_distribution.csv
  -t /path_to_input/tree_distribution.tre
  -p /path_to_input/plotting_tree.tre
  -n 1
  -o likelihood
  -s /path_to_BayesTraits/BayesTraitsV2
  -v True
```
###### 4. Visualize the character state reconstruction results via [TreeGraph2](http://treegraph.bioinfweb.info/)
```
python2.7 /path_to_git/WARACS/WARACS_TreeGraph2.py
  -r /path_to_input/tree_distribution__Mesquite_likelihood_char2.csv
  -p /path_to_input/tree_distribution__Mesquite_likelihood_char2.tre
  -c /path_to_input/color_dictionary.csv
  -s /path_to_TreeGraph2/TreeGraph.jar
  -v True
```
### - Special Notes for Windows operating systems
###### 1. Installation
* Users on Windows need to have administrative rights on their systems.
* Users on Windows need to ensure that the Python directory *Scripts* is part of the PATH environment (https://pythonhosted.org/setuptools/easy_install.html#executables-and-launchers).
* Users on Windows may need to install the latest Microsoft Visual C++ Compiler in order to successfully install the Python package *numpy* (http://stackoverflow.com/questions/28413824/installing-numpy-on-windows).

###### 2. Basic Usage
* Usage follows the following format:
```
C:\Python27\python.exe \path_to_git\WARACS\WARACS_Mesquite.py -h
```
