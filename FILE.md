# Technical specification of SDN server nodes and switches
## Server node description
### General description
| Node  | Number of CPUs | CPU model name  | RAM in kB |Server model  |Number of NICs|
| ------| -------------- | --------------- | ----------| -------------| ------------- |
|sandie-1.ultralight.org|32 |Intel(R) Xeon(R) CPU E5-2667 v3 @ 3.20GHz|264010156|SYS-2028U-TN24R4T+|6|
|sandie-3.ultralight.org|32 |Intel(R) Xeon(R) Silver 4110 CPU @ 2.10GHz|97596904| SYS-6029UZ-TR4+|6|
|sandie-4.ultralight.org|32|Intel(R) Xeon(R) Silver 4110 CPU @ 2.10GHz|97605804|SYS-6029UZ-TR4+|5|
|sandie-5.ultralight.org|64|AMD EPYC 7551P 32-Core Processor|263984632|`EMPTY`|4|
|sandie-6.ultralight.org|64|AMD EPYC 7551P 32-Core Processor|263984912|`EMPTY`|5-4|
|sandie-7.ultralight.org|96|AMD EPYC 7F72 24-Core Processor|528208900|AS -1124US-TNRP|8|
|`sandie-9.ultralight.org`||
|sandie-10.ultralight.org|32|Intel(R) Xeon(R) CPU E5-2667 v3 @ 3.20GHz|131916724 |PowerEdge R730xd|8|
|sdn-dtn-1-7.ultralight.org|20|Intel(R) Xeon(R) CPU E5-2687W v3 @ 3.10GHz|131895156|SYS-2028U-TN24R4T+|6|
|sdn-dtn-2-09.ultralight.org|40|Intel(R) Xeon(R) CPU E5-2690 v2 @ 3.00GHz|131975608|X9DRX+-F|4 +1 unclaimed (does not have MAC address too)|
|sdn-dtn-2-10.ultralight.org|28|Intel(R) Xeon(R) CPU E5-2697 v3 @ 2.60GHz|32760528|X10DRi (072815D9)|6|
|sdn-dtn-2-11.ultralight.org|28|Intel(R) Xeon(R) CPU E5-2697 v3 @ 2.60GHz|65841684|X10DRi (072815D9)|4+1 unclaimed (does not have MAC address too)|
|sdn-login-1.ultralight.org |32|Intel(R) Xeon(R) CPU E5-2670 0 @ 2.60GHz|65921748|X9DRH-7TF/7F/iTF/iF|2|

### NIC description
| Node  | Number of NICS | Capacity  | Product/Vendor |
| ------| -------------- | --------------- | ----------|
|sandie-1.ultralight.org|4|10Gbit/s|Ethernet Controller X550 /Intel Corporation|
||2||MT27700 Family [ConnectX-4] /  Mellanox Technologies|
|sandie-3.ultralight.org|4|1Gbit/s|I350 Gigabit Network Connection / Intel Corporation|
||2||MT27500 Family [ConnectX-3] /  Mellanox Technologies|
|sandie-4.ultralight.org|4|1Gbit/s|I350 Gigabit Network Connection / Intel Corporation|
||1||MT27700 Family [ConnectX-4] /  Mellanox Technologies|
|sandie-5.ultralight.org|2|1Gbit/s|NetXtreme BCM5720 Gigabit Ethernet PCIe / Broadcom Inc. and subsidiaries|
||2|| MT28800 Family [ConnectX-5 Ex] / Mellanox Technologies|
|sandie-6.ultralight.org|2|1Gbit/s|NetXtreme BCM5720 Gigabit Ethernet PCIe / Broadcom Inc. and subsidiaries|
||2|| MT28800 Family [ConnectX-5 Ex] / Mellanox Technologies|
|sandie-7.ultralight.org|2|10Gbit/s|Ethernet Controller X710 for 10GBASE-T / Intel Corporation|
||2|10Gbit/s|Ethernet Controller X710 for 10 Gigabit SFP+ / Intel Corporation|
||2|| MT28800 Family [ConnectX-5 Ex] / Mellanox Technologies|
||2|| MT28908 Family [ConnectX-6] / Mellanox Technologies|
|`sandie-9.ultralight.org`||
|sandie-10.ultralight.org|4|| MT28800 Family [ConnectX-5 Ex] / Mellanox Technologies|
||2|10Gbit/s|NetXtreme II BCM57800 1/10 Gigabit Ethernet / Broadcom Inc. and subsidiaries|
||2|1Gbit/s|NetXtreme II BCM57800 1/10 Gigabit Ethernet / Broadcom Inc. and subsidiaries|
|sdn-dtn-1-7.ultralight.org|4|10Gbit/s|Ethernet Controller X550 /Intel Corporation|
||2||MT27700 Family [ConnectX-4] /  Mellanox Technologies|
|sdn-dtn-2-09.ultralight.org|2|1Gbit/s|I350 Gigabit Network Connection / Intel Corporation|
||1|| MT27500 Family [ConnectX-3] /  Mellanox Technologies|
||1 (Unclaimed)||MT26448 [ConnectX EN 10GigE, PCIe 2.0 5GT/s] /Mellanox Technologies|
||1|10Gbit/s|
|sdn-dtn-2-10.ultralight.org|2|| MT28800 Family [ConnectX-5 Ex] / Mellanox Technologies|
||2|1Gbit/s|I350 Gigabit Network Connection / Intel Corporation|
||1||MT26448 [ConnectX EN 10GigE, PCIe 2.0 5GT/s] /Mellanox Technologies|
||1|10Gbit/s|
|sdn-dtn-2-11.ultralight.org|2|| MT28800 Family [ConnectX-5 Ex] / Mellanox Technologies|
||1 (Unclaimed)||MT26448 [ConnectX EN 10GigE, PCIe 2.0 5GT/s] /Mellanox Technologies|
||2|1Gbit/s|I350 Gigabit Network Connection / Intel Corporation|
|sdn-login-1.ultralight.org |2|1Gbit/s|I350 Gigabit Network Connection / Intel Corporation|

## SDN-Switch description

| Switch  | OS version| System Type/model number  |
| ------| -------------- | --------------- |
|Dell Z9100 (main)|Dell EMC 2.0|Z9100-ON|
|Arista|
|SONIC|SONiC-OS-master.86916-a5018e73a|MSN3700-VS2R|
|BUR0002((Wedge100BF32X)|freeRouter v22.9.28-cur|
|BUR0051 (Wedge100BF32QS)|freeRouter v22.9.28-cur|
|BUR0061 (AS9516_32D (TOFINO2)|
|BUR0001 (Wedge100BF32X)|freeRouter v22.9.28-cur|





























































