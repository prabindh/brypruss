brypruss
========

PRUSS on the Browser

Based on the Qt5 webkit2/ B2G work on AM335x, an effort is made to run Python based PRU control from within a browser.

Current status:

1. Unable to get brython to load pypruss module (.so) as it looks only for .js files. This seems to be a limitation of brython.

2. Unable to get PRU basic examples to run, as no interrupt seems to occur from PRU, even with normal Python run. This must be a solvable problem as there are examples out there in the wild, confirmed working.

Dependencies:

1. Qt5 Webkit2 (Refer http://www.gpupowered.org/node/15), or B2G browser

2. AM335x platform - either EVM/SK/ or Beaglebone

3. Kernel compiled with below options

 CONFIG_UIO=y 
 CONFIG_UIO_PRUSS=y 

4. pypruss package from 

https://intelligentagent@bitbucket.org/intelligentagent/pypruss.git

5. Brython package from

http://brython.info/index_en.html

How to run:

After ensuring regular run via Python invocation works, try it on browser.

Place all the required files (.bin, .so) in same folder of Brython.

$$ cd Brython

$$ QtTestBrowser -platform minimalegl ./pru-test.html


