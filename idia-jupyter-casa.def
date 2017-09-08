# URL: https://github.com/aardk/jupyter-casa
# Definition file for IDIA Jupyter Casa 
BootStrap: docker
From: penngwyn/jupytercasa

%runscript
	#!/bin/sh
	/usr/bin/python "$@"
%post 
	# Install some software 
	apt-get -y install wget vim python-pip 
	
	# Bind through IDIA volumes to the container
	mkdir /users /scratch /data

%environment 
	PYTHONPATH="/home/jupyter/.local/lib/python2.7/site-packages/:/usr/local/lib/python2.7/site-packages:/usr/local/casa/linux64/python/2.7"
	LD_LIBRARY_PATH="/usr/local/casa/linux64/lib" 
	CASAPATH="/usr/local/casa/ linux64" 
	PATH="/usr/local/casa/linux64/bin:$PATH" 
