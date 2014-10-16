# BIOMD0000000020: hhsa_1952

## Installation

Download this repository, and install with distutils

`python setup.py install`

Or, install using pip

`pip install git+https://github.com/biomodels/BIOMD0000000020.git`

To install a specific version (in this example, from the 2014-09-16 BioModels release)

`pip install git+https://github.com/biomodels/BIOMD0000000020.git@20140916`

## Usage

Importing the model package.

`import BIOMD0000000020 as model`

Get the SBML string from the model

`print model.sbmlString`

If [python-libsbml](https://pypi.python.org/pypi/python-libsbml) bindings are
installed, the libsbml.SBMLDocument object is also accessible

`model.sbml`


# Model Notes


This is an implementation of the Hodgkin-Huxley model of the electrical
behavior of the squid axon membrane from:  
**A quantitative description of membrane current and its application to conduction and excitation in nerve.**   
A. L. Hodgkin and A. F. Huxley. (1952 ) _Journal of Physiology_ 119(4): pp
500-544; pmID: [12991237](http://www.ncbi.nlm.nih.gov/pubmed/12991237) .  

**Abstract:**   
This article concludes a series of papers concerned with the flow of electric
current through the surface membrane of a giant nerve fibre (Hodgkin,Huxley &
Katz, 1952; Hodgkin & Huxley, 1952 a-c). Its general object is to discuss the
results of the preceding papers (Part I), to put them into mathematical form
(Part II) and to show that they will account for conduction and excitation in
quantitative terms (Part III).

This SBML model uses the same formalism as the one described in the paper,
contrary to modern versions:  
* V describes the the membrane depolarisation relative to the resting potential of the membrane   
* opposing to modern practice, depolarization is _negative_ , not _positive_ , so the sign of V is different   
* inward transmembrane currents are considered positive (inward current positive), contrary to modern use   
The changeable parameters are the equilibrium potentials( _E_R, E_K, E_L,
E_Na_ ), the membrane depolarization ( _V_ ) and the initial sodium and
potassium channel activation and inactivation coefficients ( _m,h,n_ ). The
initial values of _m,h,n_ for the model were calculated for _V_ = 0 using the
equations from the article: _n t=0 = α_n V=0 /(α_n V=0 \+ β_n V=0 ) _ and
equivalent expressions for _h_ and _m_ .  
For single excitations apply a negative membrane depolarization (V < 0). To
achieve oscillatory behavior either change the resting potential to a more
positive value or apply a constant negative ionic current (I < 0).  
Two assignments for parameters in the model, alpha_n and alpha_m, are not
defined at V=-10 resp. -25 mV. We did not change this to keep the formulas
similar to the original publication and as most integrators seem not to have
any problem with it. The limits at V=-10 and -25 mV are 0.1 for alpha_n resp.
1 for alpha_m.  
We thank Mark W. Johnson for finding a bug in the model and his helpful
comments.

This model originates from BioModels Database: A Database of Annotated
Published Models. It is copyright (c) 2005-2009 The BioModels Team.  
For more information see the [terms of
use](http://www.ebi.ac.uk/biomodels/legal.html) .  
To cite BioModels Database, please use [Le Novère N., Bornstein B., Broicher
A., Courtot M., Donizelli M., Dharuri H., Li L., Sauro H., Schilstra M.,
Shapiro B., Snoep J.L., Hucka M. (2006) BioModels Database: A Free,
Centralized Database of Curated, Published, Quantitative Kinetic Models of
Biochemical and Cellular Systems Nucleic Acids Res., 34: D689-D691.](http://ww
w.pubmedcentral.nih.gov/articlerender.fcgi?tool=pubmed&pubmedid=16381960)


