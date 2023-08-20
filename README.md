# Image-Encryption-using-Modified-SNOW-3G-Algorithm
This is a research-based project using a modified SNOW 3G algorithm.
The aim of the project is to secure and protect sensitive visual information
It converts the image into encrypted form that can only be accessed and understood by authorised systems


INTRODUCTION
In today's world, digital images play a critical role in multimedia communications that are happening at a
breakneck pace because of Internet of Things (IoT) applications. However, if the data is sensitive, it is critical to
ensure its protection. Even though the Internet of Things architecture provides numerous advantages to
humanity, data transfers pose various security threats, particularly when sensitive images are transferred. These
sensors gather data from their surroundings and broadcast it across unsecured public networks. In this context,
the adversary can play a crucial role in taking advantage of the system by manipulating the data via various
security attacks. As IoT application sensors have some storage and computation constraints, providing security
to those applications becomes difficult. Traditional ciphers, as a result, cannot be utilized in IoT devices.
SNOW 3G Algorithm , on the other hand, may be used to provide security to IoT devices in this resourceconstrained context because this stream cipher is capable of constructing complicated patterns and pseudorandom sequences efficiently at high speed. It is also simple to put into hardware. Role of cloud-based IoT
infrastructure is vital in the present digital world. In this configuration, small devices use sensors to collect data
and send it over the Internet to cloud storage servers.
These data are utilized for further analysis and processing at the application layer [1]. Actuators and sensors are
deployed at the perception layer [2]. In contrast, gateway devices with some computational capabilities are
installed at the network layer in a typical IoT network scenario. These sensors collect data from regions humans
cannot observe directly. In the application layer, users are allowed to interact with the cloud. Many traditional
ciphers are available to maintain information security at the network or application layers. However, these
cannot be used at the perception layers due to the resource limits of the sensory equipment. As a result, a fast
and lightweight encryption technique in the perception layer.
Word Oriented Stream cipher [3,4,5] plays an important role in modern day communication. In 4G and 5G
communications, SNOW 3G [6] cipher is used to keep the confidentiality and integrity of the data. Moreover, it
gives 128−bit security, and it has high throughput. It can be used efficiently in hardware, software or embedded
system devices. In short, the major contributions of this work are listed below:
● A modified SNOW 3G KSG by changing the Linear Feedback Shift Register (LFSR) with 64 inputoutput, 8 delay blocks σ−LFSR is proposed. A feedback configuration matrix [7,8] has been used
instead of the feedback matrix of SNOW 3G to reduce the encryption time of traditional cipher and
enhance the randomness of the keystream.
● Security aspect of the KSG is proved theoretically. Furthermore, the randomness of the proposed KSG
is evaluated by the NIST randomness test suit.
● Proposed image encryption scheme is validated by standard tests like information entropy test,
histogram analysis, correlation coefficients, NPCR, UACI etc
