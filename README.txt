Overview
========

ohconvert integrates ohcount_ into Jenkins_.

This script invokes ohcount, parses its output and converts it into the format
understood by the SLOCCountPlugin_ for Jenkins. This is equivalent to calling
sloccount_ with the options::

    sloccount --duplicates --wide --details path ...

Prerequisites
-------------

You need to have ohcount_ 3.0.0 or later installed and it needs to be directly
executable from the path. You can check by calling ``ohcount --help``. ohcount
can be built manually or is available from some system package management tools.
For example it's available as ``ohcount`` in the latest macports_.

Usage
-----

You can call the script via::

    ohconvert path ...

Output Jenkins SLOCCountPlugin compatible data collected with ohcount.

Options:

* `-h, --help` show this help message and exit
* `-o sloccount.sc, --output=sloccount.sc` Output filename (instead of stdout)

Development
-----------

The source code can be found at: https://github.com/hannosch/ohconvert


.. _ohcount: http://ohcount.sourceforge.net/
.. _Jenkins: http://jenkins-ci.org/
.. _sloccount: http://www.dwheeler.com/sloccount/
.. _SLOCCountPlugin: http://wiki.jenkins-ci.org/display/JENKINS/SLOCCount+Plugin
.. _macports: http://www.macports.org/
