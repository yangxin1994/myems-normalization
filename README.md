## MyEMS Normalization Service 数据规范化服务



### Introduction

This service is a component of MyEMS and it normalizes energy data in historical database.




### Prerequisites

mysql.connector

sympy

openpyxl


### Installation
    1. Install MySQL Connector
```
    $ pip3 install mysql-connector-python
```
    2. Install mpmath
```
   $ sudo pip3 install mpmath
```
    3. Install SymPy
```
    $ git clone https://github.com/sympy/sympy.git
    $ cd sympy
    $ sudo python3 setupegg.py develop
```
    4. Install openpyxl
```
    $ sudo pip3 install openpyxl
```
    5. Install myems-normalization service:
```
    $ cd ~/myems-normalization
    $ sudo cp -R ~/myems-normalization /myems-normalization
    $ cd /myems-normalization
```
    Edit config.py for your project
```
    $ sudo nano config.py
```
    Setup systemd configure files:
```
    $ sudo cp myems-normalization.service /lib/systemd/system/
```
    Next enable the services so they autostart at boot:
```
    $ sudo systemctl enable feed-normalizing.service
```
    Either reboot, or start the services manually:
```
    $ sudo systemctl start feed-normalizing.service
```

### References

1. https://myems.io
2. https://dev.mysql.com/doc/connector-python/en/
3. https://github.com/sympy/sympy
4. https://openpyxl.readthedocs.io
