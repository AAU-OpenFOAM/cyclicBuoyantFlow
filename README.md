# cyclicBuoyantFlow

cyclicBuoyantFlow solves cases for buoyant, incompressible, turbulent flow. 

## Compatibility:

The solver is known to work using the following OpenFOAM versions:

8, 9

Other versions are not supported directly. Let me know and I'll be happy to update it to a newer version.

## Installation:

0.  Source your OpenFOAM environment, e.g.: 

        source /home/$USER/OpenFOAM/OpenFOAM-9/etc/bashrc

1.  In a linux terminal download the package with git by typing:

        git clone https://github.com/AAU-OpenFOAM/cyclicBuoyantFlow.git

2.  Execute the Allwmake script by typing (will finish in ~1 minute):

        cd cyclicBuoyantFlow
        ./Allwmake

    The solver will be compiled to your $FOAM_USER_APPBIN (you can check where e.g. the environmental 
    variable $FOAM_USER_APPBIN points to by typing in the terminal:

        echo $FOAM_USER_APPBIN
    
3.  Test installation with a simple test case by typing (finishes in secs):

        cd testCase
        ./Allrun
	
    Run the Python script (testCase/postProcess.py) to view the velocity profile along with the analytical solution
    
        python postProcess.py

## Addtional keywords:

The following lists additional keywords that have to be specified by the user:

      "constant/transportProperties"
      {
          ?
      }

## Developers:

* Jakob Hærvig (conceptualise, code developer, maintainer)
