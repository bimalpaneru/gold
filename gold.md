## Removing Python package manually
```
--------------------------------------------------------------------------
## Find the package location

$ python3

>> import module name as m
>> print(m.__file__)

--------------------------------------------------------------------------
## Usually stored in /home/bimal/.local/lib/python3.10/site-packages/setuptools/
## Remove this file

$ rm -r /home/bimal/.local/lib/python3.10/site-packages/setuptools/
--------------------------------------------------------------------------
## Remove the eff.info file which makes pip to not identify the package and assumed it is removed
## egg.info file might require change of permission

$ sudo chmod 777 /home/bimal/.local/lib/python3.10/site-packages/setuptools-egg.infoXX/

$ rm -r /home/bimal/.local/lib/python3.10/site-packages/setuptools-egg.infoXX/ file
--------------------------------------------------------------------------
```
