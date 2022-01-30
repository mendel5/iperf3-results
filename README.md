# iperf3-results
Interpretation of iperf and iperf3 results, especially regarding speed.

## Bandwidth
After testing my connection with iperf3, I was wondering if my results are good and what a good/ acceptable bandwidth looks like.
The iperf3 test was done with a CAT6 cable that supports gigabit ethernet. iperf3 was running in TCP mode.

I found the following references.

### Reference 1
> iperf indicating 940 Mbits/sec using cat 5 cable

> ~943 megabits per second is the theoretical max throughput you can get with TCP over IPv4 over 1000BASE-T using standard 1500 byte payloads, because of mandatory inter-packet gaps and other protocol overhead. So you're seeing full speeds as expected. 

Source:
- https://superuser.com/questions/1417479/iperf-indicating-940-mbits-sec-using-cat-5-cable

### Reference 2
> Proving the Network is Not the Problem With iperf

> From the output above we see that the lowest observed throughput within a one-second interval was 927 Mbps, with an average rate of 939 Mbps. These numbers approach the maximum practical throughput for a 1 Gbps Ethernet link, and strongly suggest that the network is not at fault.

Source:
- https://packetlife.net/blog/2011/feb/28/proving-network-not-problem-iperf/

### Reference 3
> Iperf testing. What is considered a good result on a Gigabit network?

> You should get around 940 Mbps if everything is working properly and you don't have any bottlenecks.

Source:
- https://www.reddit.com/r/HomeNetworking/comments/70sai8/iperf_testing_what_is_considered_a_good_result_on/
- https://www.reddit.com/r/HomeNetworking/comments/70sai8/iperf_testing_what_is_considered_a_good_result_on/dn5kmuy/

### Reference 4
> Using Iperf for measuring the network speed

> The following stats show actual iperf measurements. Measurements were taken on a classic Ethernet hub, a Fast Ethernet switch and a Gigabit Ethernet. Iperf was first started without further options and then with the command `iperf -c 192.168.0.20 -w 512k -l 512k`.

| Network type     | Iperf default [MBit/s] | Iperf with options (see above) [MBit/s] | Theoretical maximum [MBit/s] |
|------------------|------------------------|-----------------------------------------|------------------------------|
| Ethernet hub     | 7,5                    | 7,5                                     | 10                           |
| Fast Ethernet    | 95                     | 95                                      | 100                          |
| Gigabit Ethernet | 346                    | 948                                     | 1000                         |

> The measurements were performed between two systems with Intel Core 2 Duo CPU at around 2 GHz. Broadcom NetXtreme Gigabit NICs were used as network cards. The combination of Thinkpad R60 (Windows XP) and Apple Mac Mini C2D 1.83 MHz (Mac OS X Leopard) achieved about 940 MBit/s in the test.

Source:
- http://www.nwlab.net/art/iperf/


### Tags
- Expected bandwidth
- data transfer rate
- Is my bandwidth ok?
- Are my results good?
- iperf3 expected results
- iperf3 good results example


## Commands

```
iperf3 -s -V
```

This command starts iperf3 in server mode. The `-s` activates the server mode and the `-V` is for enabling the detailed output (verbose). Other commands can be found with `iperf3 help`.

```
iperf3 -s -V > ~/iperf3-log.txt
```

This command does the same thing as the one above, except that it writes the output to the file `iperf3-log.txt` in the user's home directory in contrast to printing it on the console/ terminal (as the first command does).
