# Infrastructure Benchmarks

All benchmarks are performed using industry-standard testing scripts on idle machines. Network speeds may vary slightly depending on peak datacenter routing, but 1 Gbit/s is unmetered and guaranteed at the switch port.

```text
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #
#              Yet-Another-Bench-Script              #
#                     v2026-08-30                    #
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #

Sun Aug 30 14:02:15 CEST 2026

[1] TARGET: DUPE-1 (Offshore Dedicated Bare-Metal)
----------------------------------------------------------------------
Basic System Information:
---------------------------------
Uptime     : 30 days, 1 hours, 19 minutes, 7 seconds
Processor  : AMD Ryzen 7 9700X 8-Core Processor
CPU cores  : 16 @ 3800.000 MHz (Boost: 5500.000 MHz)
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 62.7 GiB (DDR5 5200 MHz On-Die ECC)
Swap       : 2.0 GiB
Disk       : 931.5 GiB (2x 512 GB NVMe SSD - Soft RAID 0)
OS         : Debian GNU/Linux 12 (bookworm) x86_64

fio Disk Speed Tests (Mixed R/W 50/50) (Partition /dev/md0):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------   | ---            ----  | ----           ----
Read       | 1.35 GB/s   (337.5k) | 7.12 GB/s   (111.2k)
Write      | 1.35 GB/s   (337.5k) | 7.15 GB/s   (111.7k)
Total      | 2.70 GB/s   (675.0k) | 14.27 GB/s  (222.9k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location          | Send Speed      | Recv Speed     | Ping
-----           | -----             | ----            | ----           | ----
Clouvider       | London, UK        | 941 Mbits/sec   | 939 Mbits/sec  | 4.12 ms
Scaleway        | Paris, FR         | 942 Mbits/sec   | 942 Mbits/sec  | 2.45 ms
Novoserve       | North Holland, NL | 938 Mbits/sec   | 935 Mbits/sec  | 6.78 ms

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value
                |
Single Core     | 3245
Multi Core      | 16120


======================================================================


[2] TARGET: HIGH-PERFORMANCE VDS (8GB RAM | 4vCPU)
----------------------------------------------------------------------
Basic System Information:
---------------------------------
Uptime     : 30 days, 1 hours, 19 minutes, 7 seconds
Processor  : AMD EPYC-Milan Processor (Virtual)
CPU cores  : 4 @ 3200.000 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ❌ Disabled
RAM        : 7.8 GiB
Swap       : 1.0 GiB
Disk       : 98.5 GiB (NVMe Virtual Block)
OS         : Ubuntu 22.04.4 LTS x86_64

fio Disk Speed Tests (Mixed R/W 50/50) (Partition /dev/sda1):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------   | ---            ----  | ----           ----
Read       | 450 MB/s    (112.5k) | 1.82 GB/s    (28.4k)
Write      | 450 MB/s    (112.5k) | 1.82 GB/s    (28.4k)
Total      | 900 MB/s    (225.0k) | 3.64 GB/s    (56.8k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location          | Send Speed      | Recv Speed     | Ping
-----           | -----             | ----            | ----           | ----
Scaleway        | Paris, FR         | 935 Mbits/sec   | 920 Mbits/sec  | 2.50 ms
Clouvider       | London, UK        | 910 Mbits/sec   | 890 Mbits/sec  | 4.25 ms

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value
                |
Single Core     | 1450
Multi Core      | 4890
