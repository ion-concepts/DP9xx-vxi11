# DP9xx-vxi11
Python Application to control Rigol DP9xx PSU using python leveraging vxi11 library

## Example
ianb@cruncher:~/rigol$ python3
Python 3.8.10 (default, Nov 22 2023, 10:22:35)
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from instruments import DP900
>>> instrument = DP900("192.168.101.120")
>>> instrument.disable_output(3)
>>> instrument.enable_output(3)
>>> instrument.measure(1)
{'voltage': Decimal('12.00'), 'current': Decimal('0.09'), 'power': Decimal('1.080')}
>>> instrument.measure(2)
{'voltage': Decimal('23.99'), 'current': Decimal('1.10'), 'power': Decimal('26.388')}
>>> instrument.measure(3)
{'voltage': Decimal('5.00'), 'current': Decimal('0.00'), 'power': Decimal('0.000')}
>>> quit()

