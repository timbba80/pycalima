========
PyCalima
========

Simple python interface against the
`Pax Calima® <http://www.pax.se/sv/produkt/calima/pax-calima-flakt>`_
bathroom fan created and sold by `Pax® <http://www.pax.se>`_

This module provides a very simple interface against the various
GATT characteristics of the Calima fan, most importantly it handles the
authentication so values are actually persisted within the fan.

Uses `BluePy <https://github.com/IanHarvey/bluepy>`_


========
Installation from Pypi: 
========

```
python3 -m pip install calima
```

========
Manual Installation
========

1. Install python3:

```
$apt install python3 python3-pip libglib2.0-dev
```

2. Then install BluePy

```
$sudo pip3 install bluepy
```


========
Demo usage
========


```code:: python```

```from Calima import Calima```

```fan = Calima("MA:CC:AD:DR:ES:SS", "012345")```
```print(fan.getAlias())
```


========
Command line tool
========

Pretty useful command line tool which among other things can print all
the characteristics of a fan. It can also search for available fans 
if you don't know the MAC address.

For more on using the tool, just run `calima -h`.


========
Debugging
========

Set this to True in pycalima/Calima.py file if want to see more verbose output.

```
self._debug = False
```

========
Documentation
========

A good readup introductory readup on BLE reverse engineering can be found
`here <https://medium.com/@urish/reverse-engineering-a-bluetooth-lightbulb-56580fcb7546#.9ltnsvdsn>`_.

Some badly structured details about the protocol can be found in the
`Characteristics file <characteristics.md>`_.

There is currently no documentation on the module yet, check the
Calima.py file to see available functions.

========
License
========

See LICENSE file
