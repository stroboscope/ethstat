# ethstat

Tool to dynamially observe current ethernet statistics in simple and readable
form. It reads hardware stat from `ethtool -S` and display in table format (for
queues), additional line for scalar stats where errors marked with red color.

### Example output
```
   -16:04.34- :     rx   rx-0   rx-1   rx-2   rx-3     tx   tx-0   tx-1   tx-2   tx-3 (gate2)
 eth0  packets:  17882   3386   2966   5224   6295  23525    1.9  23519    1.9      0
 eth0 tx_broadcast: 1.9 rx_multicast: 1.9
 eth2  packets:  17726   4080   5232   4438   3978  17835      0  17831      0      0
 eth3  packets:  27075   5439   6574   6943   8119  17667      0  17666      0      0
 eth3 csum_err:             0      0    1.9      0
```
All numbers are usually packet related *per-second rates*. Thats why you will
see floating point numbers sometimes.

### Options
* `-e` to show only error stats (default is everything, except redundant data).
* `-b` to show also byte counters (default only packets).
* `-h` for help.

### Requires
*ruby* 1.8 or higher.

### License
GPL

(c) 2014, abc @ telekom.ru.

