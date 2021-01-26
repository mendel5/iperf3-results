# iperf3-results
Results of iperf and iperf3

## Bandwidth
After testing my connection with iperf3 I was wondering if my results are good and what a good/ acceptable bandwidth looks like. I found the following references.

The iperf3 test was done with a CAT6 cable that supports gigabit ethernet. iperf3 was running in TCP mode.

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


Tags:
- Expected bandwidth
- data transfer rate
- Is my bandwidth ok?
- Are my results good?
