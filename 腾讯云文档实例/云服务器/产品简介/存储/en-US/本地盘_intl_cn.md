## Overview
This site is a storage device on the same physical server as the cloud server instance, with high read and write IO, low latency characteristics.
This site is from the local storage of the physical machine where the CVM instance resides and is a storage area divided from the physical machine on which the CVM instance resides. Both the system disk and the data disk support the selection of this site, and only the selection of SSD local disks is supported when purchasing high IO models.
**Life cycle: **The creation of this site follows only the cloud server instance. As a result, this site starts or terminates following the lifecycle of the cloud server.
**Buy: **This site can only be started together when the cloud server is started. Therefore, the purchase of this site can only be specified when purchasing a cloud server instance. For more information about purchasing a cloud server, please refer to the [Buy and start an instance](/doc/product/213/4855)。
>**Attention:**
&gt; Select the cloud server for this site does not support hardware (CPU, memory) upgrades, only bandwidth upgrades are supported.
## Type
This site is a local storage from the physical machine where the cloud server is located, and can be divided into normal local disks and SSD local disks depending on the media.
### Normal Local Disk
<table class="typical">
	<tbody>
	<tr>
		<th>Specifications</th>
		<th>Buying strategy</th>
		<th>Performance</th>
		<th>Price</th>
	</tr>
	<tr>
		<td rowspan="2">System disk</td>
		<td>Linux Systems: Complimentary GB capacity, you can choose to purchase a larger capacity, the maximum support of GB.</td>
		<td rowspan="3">Peak throughput of more than 40-100 mb/s,iops hundreds of to 1000</td>
		<td rowspan="3">Package Year Monthly: 0.3 Yuan/gb/months<br>Billing by Volume: 0.042 Yuan/100 g/hours</td>
	</tr>
	<tr>
		<td>Windows System: Complimentary $ GB capacity, cannot be changed.</td>
	</tr>
	<tr>
		<td>Data disk</td>
		<td>Supports a normal local disk specification of a minimum of up to 1000 GB to a maximum of $ (with a size of $ G), and different hardware configurations have different limits for normal local disks.</td>
	</tr>
</tbody></table>
### SSD Local Disk
The SSD local disk is a local storage from the physical machine where the cloud server resides, which provides block-level data access for instances with low latency, high random IOPS, and high throughput I/O capabilities.
<table class="SSD">
	<tbody>
	<tr>
		<th>Specifications</th>
		<th>Buying strategy</th>
		<th>Performance</th>
		<th>Price</th>
	</tr>
	<tr>
		<td rowspan="2">System disk</td>
		<td>Linux Systems: Complimentary 20GB capacity, cannot be changed.</td>
		<td rowspan="3">Throughput Peak 290 mb/s (4K Random Read), IOPS 75000 (4K Random Read Depth-32), access delay less than 3 ms</td>
		<td rowspan="3">Package Year Monthly: 0.8 yuan/gb/months<br/>Billing by Volume: 0.33 Yuan/100G/hours</td>
	</tr>
	<tr>
		<td>Windows System: Complimentary 50GB capacity, cannot be changed.</td>
	</tr>
	<tr>
		<td>Data disk</td>
		<td>Supports SSD local disk specifications with a minimum of 10GB to a maximum of 250GB (with 10G as step length), and different hardware configurations have different limits for normal local disk specifications.</td>
	</tr>
</tbody></table>
The SSD local disk is suitable for use in the following scenarios:
- Low latency: Provides a microsecond level of access delay. 
- Distributed Applications: I/O-intensive applications such as NoSQL, MPP data warehouses, Distributed file systems, which themselves have distributed data redundancy capabilities. 
- Large online Application logs: Large online applications generate large amounts of log data and require high-performance storage, while log data requires less reliability for storage. 
- Single point of risk: There is a single point of failure risk, it is recommended to do data redundancy in the application layer to ensure data availability.
