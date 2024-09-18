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


## Platformio cannot find the interpreter
```
# Likely venv is not installed install it using
-----------------------------
$ sudo apt install python3-venv
```


## Foxy-Proxy connect to remote machine to access services
```
# From your localhost bind the address to a port
$ ssh -D 5050 user@remote-hostname

# Use this settings on the foxyproxy
Hostname: locahost
Port: 5050
Type: SOCKS4
```


## Read  data on a port using `socat`
`$ socat - TCP:<hostip>:<port>`
