# NetworkPractice

***
***Note: The information provieded might have wrong or unprecise information, its always on you to keep diving into the concepts, and find the real correct and precise knowledege.***
***
![Logo](Img/NetPractice.png)
***

***Net Practice, 42 Project aimed to understand TCP/IP, OSI Model and sub-netting, theoretically and by practice using sub-netting exercises simulations.***
***

#### What is Subnetting ?

According to a well known resource, **Cloudflare**, a subnet, or subnetwork, is a **Network** inside a network, subnets make networks more efficient.
Through subnetting, network traffic can travel a shorter distance without passing through unnecessary routers to rach its distination.

#### How does devices communicates? What is the OSI Model?

**OSI Model** or Open systems interconnection model, is a conceptual framework used to understand and design how different computer systems communicate over a network.
By deviding the network communication into seven distinct layers, each specific layer has its own functionality, enabling various hardware and software componenets to interoperate and exchange data effectively.

### **OSI Model Layers**

##### **➤ Physical Layer**:
the main role of this layer, is to transmit raw bits **[0|1]**, from one device to another over a physical medium such as wires, fiber optics or wireless channels, this layer is responsible for converting the digital data into signals suitable for transmission (encoding/modulation) and converting recieved signals back into data (decoding/demodulation).

**What is encoding/modulation ?**

Encoding and modulation are two fundamental processes at the physical layer of the **OSI Model**, that prepare digital data for transmission over physical media;

###### **Encoding:**
encoding is the process of converting raw digital bits [0|1], into a specific pattern of signals that can be transmitted across a physical medium, the encoded signals represent the bits in a way suitable for the transmission environment, ensuring proper synchronization between sender and reciever...{to complete !}
Various encoding schemes exist, such as:

* ***Non-Return-to-Zero (NRZ)***: Uses two voltage levels representing 0 and 1 without returning to zero between bits, meaning if we have [110],
the singal voltage stays high throughout all two bits without dropping to zero in between, and then stays low for the next last bit.
In this type of scheme there is no neutral zero return for the voltage as its stay at the voltage represented by the passing bits.
There different types of the NRZ but the primary two types of NRZ are [NRZ-I/NRZ-L], for further more understanding, here is a Youtube video explaining NRZ-I and how it works: [NRZ-I](https://www.youtube.com/watch?v=Kxndom8GaUQ)

* ***Manchester Encoding***: The direction of a transition between positive and negative voltage in the middle of the bit time represents the data.
In this type of encoding, there is two type conventions for representing binary data, **BIPHASE-L (Mancherser II)** and **IEEE 802.3 / IEE 802.4**.

This is the first convention **BIPHASE-L**:
***
![Logo](Img/ManchesterEncoding.png)
***

the **IEEE 802.3 / IEE 802.4** is the opposite of the above convention.
for further more understanding, here is a Youtube video explaining **BIPHASE-L (Mancherser II)** and how it works: [Mancherser II](https://www.youtube.com/watch?v=J00Hfx-tF-U)

**Note**:
The reciever of the coming data, has hardware decives called **Network Interface Cards** **(NICs)** that are designed and programmed to catch, interpret, decode and demodulate the physical signals into digital bits based on the encoding scheme used (NRZ, Manchester...).
this **(NICs)** is controlled by firmware (low-level software) and drivers within the operating system, which manage the communication between hardware and higher-level network protocols.

###### **Modulation:**
Modulation prepares the signal for effective transmission by imprinting the encoded data onto a fast-moving carrier wave tuned to a frequency that travels well through the chosen medium, ensuring reliable reception at the other end.
The coming encoded data arrives, the modulator changes the carrier's amplitude, frequency or phase according to the encoded signal, effectively embedding the data onto this wave.
So modulation tailors the encoded digital data to physically compatible signals that can be transmitted reliably over the intended medium, this process ensures the data can travel long distances or through complexe environments while being received and decoded properly at the other end.

**How does modulation helps the data to travel safely?**:
An example of modulation functionality, is shifting the encoded data onto a high-frequency carrier wave, so it allow it to propagate further without significant loss or distortion compared to low-frequency baseband signals, higher frequency carriers suffer less attenuation, making long-distance communication possible.