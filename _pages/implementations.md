---
permalink: /activities/implementations/
title: ""
toc: True
toc_sticky: True 
toc_label: "Categories"
---

[Back] to activities

[Back]:/activities/

## Implementations

<span style="font-size:90%"> Each implementation will be shown in a nutshell. 

### 6. NS-3 Self Organized Network

<span style="font-size:80%"> Keywords: NS-3, SON, Reinforcement Learning, C++, Python.

{% include figure image_path="/assets/Implementations/SON/System Model.pdf" alt="this is a placeholder image" caption="Fig. 6-1. System Model." %}

<span style="font-size:80%"> In this system, we build the interface for SON, especially aims to adjust parameter (CellsToAddMod) based on PrbUsage.
SON server \(NS-3 Gym Part) determines the CellsToAddMod with a certain algorithm, and NetSim part periodically updates the value (i.e., PrbUsage) used to SON server.
CellsToAddMod is sent to the UE and they use this value when they conduct the handover (A3 RSRP Handover).


{% include figure image_path="/assets/Implementations/SON/Framework.pdf" alt="this is a placeholder image" caption="Fig. 6-2. Framework." %}

<span style="font-size:80%"> The SON can be consists of Open AI Gym (python) part and NS-3 part. 



{% include figure image_path="/assets/Implementations/SON/Result.pdf" alt="this is a placeholder image" caption="Fig. 6-3. Results." %}

<span style="font-size:80%"> So, In the result, Red box in \<Terminal of Son Server> shows CellsToAddMod is determined and Red box in \<Terminal of NS-3> is received and UEs recieves results. The blue box is next step and it shows the same result. 


### 5. Network Data Analytics Function (NWDAF) Using Free5GC

<span style="font-size:80%"> Keywords: NFV, NWDAF, Deep Learning, Go, Python, Free5GC.

{% include figure image_path="/assets/Implementations/NWDAF/Network Architecture.pdf" alt="this is a placeholder image" caption="Fig. 5-1. Network Architecture." %}

<span style="font-size:80%"> In free5gc, the initial network (except NWDAF) is composed of multiple network functions. And if NWDAF is added, it will be on the 5G core network.

{% include figure image_path="/assets/Implementations/NWDAF/NWDAF Architecture.pdf" alt="this is a placeholder image" caption="Fig. 5-2. NWDAF Architecture." %}

<span style="font-size:80%"> Role of NWDAF can consist of training learning model (MTLF) and inferencing data (AnLF). Therefore, if we implement the NWDAF using Free5GC, it can be devided into Free5GC module (based on Go Lang) and Learning module (based on Python). In addition, the deep learning model is implemented by Keras.

{% include figure image_path="/assets/Implementations/NWDAF/Initial State of NRF.pdf" alt="this is a placeholder image" caption="Fig. 5-3. Initial State of NRF." %}

<span style="font-size:80%"> Fig. 5-3 shows the initial state of NRF, which function did not recieved any results. Therefore, the database of NRF have any tuples for network functions.



{% include figure image_path="/assets/Implementations/NWDAF/NWDAF.pdf" alt="this is a placeholder image" caption="Fig. 5-4. Turning on NWDAF." %}

<span style="font-size:80%"> Fig. 5-4 shows when turning on NWDAF, which green box shows requesting message formats (based on URI) for processing the functions.

{% include figure image_path="/assets/Implementations/NWDAF/After Register.pdf" alt="this is a placeholder image" caption="Fig. 5-5. NRF When After Registering NWDAF." %}

<span style="font-size:80%"> After turning on NWDAF, NRF recieves message from NWDAF, which registers the information of NWDAF and database stores it. 

{% include figure image_path="/assets/Implementations/NWDAF/MTLF.pdf" alt="this is a placeholder image" caption="Fig. 5-6. Requesting MTLF." %}

<span style="font-size:80%"> Fig. 5-6 shows the MTLF process, which have 3 terminals for Free5GC Module and Learning Module in Free5GC and Requester for any other function. When requester requests MTLF to Free5GC Moudule. Then, Learning Module trains the deep learning model. 

{% include figure image_path="/assets/Implementations/NWDAF/AnLF.pdf" alt="this is a placeholder image" caption="Fig. 5-7. Requesting AnLF." %}

<span style="font-size:80%"> Fig. 5-6 shows the AnLF process, which have 3 terminals for Free5GC Module and Learning Module in Free5GC and Requester for any other function. When requester requests AnLF to Free5GC Moudule. Then, Learning Module inferences the data using deep learning model. 


### Notice for implementation number 4. to 2.



<span style="font-size:80%"> 4. Host Identity Protocol and Partially DMM (MAD-PMIPv6) integrated testbed, <br/> 3. NS-3 Tap Bridge and MAD-PMIPv6 integrated Testbed, <br/> and 2. NS-3 Simulation module for DMM based on PMIPv6 <br/> has a military secret due to its security clearance.

<span style="font-size:80%"> I am sorry for not opening them.

### 1. Static Router with GUI

<span style="font-size:80%"> Keywords: Routing

<span style="font-size:80%"> This program is implemented by Python with Qt. The routing program is operated with real devices. 

<span style="font-size:80%"> In Fig. 1-1 and Fig. 1-2, they shows the process of IP routing and ARP. Each blue box shows the routing program codes and arrows are the path of data (packets).

{% include figure image_path="/assets/Implementations/PyRouter/IP Routing Process.pdf" alt="this is a placeholder image" caption="Fig. 1-1. Process of IP Routing." %}

<span style="font-size:80%"> In Fig. 1-1, blue arrows are process of ingress packets and green arrows show process of egress. Green arrows in IP layer shows the forwarding process. Meanwhile, when cannot find mac destinaition in forwarding table (green dashed arrow), process of ARP is started. 

{% include figure image_path="/assets/Implementations/PyRouter/ARP Process.pdf" alt="this is a placeholder image" caption="Fig. 1-2. Process of ARP." %}

<span style="font-size:80%"> In the process of ARP in Fig 1-2, Meaning of Blue arrows and Red arrows are the same. 

<span style="font-size:80%"> The routing program is operate same process on these Fig. 1-1 and 1-2.

{% include figure image_path="/assets/Implementations/PyRouter/Network Topology.pdf" alt="this is a placeholder image" caption="Fig. 1-3. Network Topology." %}

<span style="font-size:80%"> The network topology is described in Fig. 1-3. Router program is on the Mac OS, which program can running on also Windows and Unix kernel (checked in Ubuntu and Raspbian).


{% include figure image_path="/assets/Implementations/PyRouter/Routing Results 1.pdf" alt="this is a placeholder image" caption="Fig. 1-4. Result: When Turning Off." %}

<span style="font-size:80%"> When turning off routing program, it did not activated so, packets sended by Raspbian cannot reached to Windows PC via Mac OS.

{% include figure image_path="/assets/Implementations/PyRouter/Routing Results 2.pdf" alt="this is a placeholder image" caption="Fig. 1-5. Result: When Turning On." %}

<span style="font-size:80%"> Meanwhile, when routing program is turning on, packets can be reached to Windows PC.

