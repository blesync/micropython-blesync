# blesync

Motivation: Original MicroPython to handle BLE communication is IRQ with callback functions [ubluetooth docs](https://docs.micropython.org/en/latest/library/ubluetooth.html). This library is to wrap this with synchronuous approach.


Comparison of scan devices procedure:

original in **ubluetooth**:

```
BLE.irq(...) - register handler `_IRQ_SCAN_RESULT` (all handlers in one function)
BLE.gap_scan(...) - returns nothing
```

our approach **blesync**:

```
blesync.scan(...) - returns iterator with the same structure as original uPy ubluetooth
```
