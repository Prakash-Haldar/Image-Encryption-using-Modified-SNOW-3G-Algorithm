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


WORKING PROCEDURES/ PROPOSED APPROACHES/ IMPLEMENTATION
Working Procedures
A Pseudo Random Number Generator (PRNG)) is a process which produces a sequence of numbers whose
properties approximate the properties of sequences of random numbers. Linear Feedback Shift Register (LFSR)
is one of the popular PRNG. It is used in Cryptography and Coding theory for its good statistical properties and
easy implementation in hardware. As it has a drawback in software implementation, Word-based LFSR is used
in modern Word-based processors. σ−LFSR is one kind of Word-based LFSR [36].
Definition 1. We dene a σ−LFSR [37] as a word based LFSR which follows the following recurrence relation,



where, each si ∈ 𝔽2
m and Ci ∈ 𝔽2
m*m. Here, each delay block has m-inputs and m-outputs and the σ-LFSR
generates a sequence of vectors in 𝔽2
m. The matrices C0, C1, · · ·, Cb−1 are referred to as the gain matrices of the
σ-LFSR and the following matrix is defined as its configuration matrix.
where, ze, Id ∈ 𝔽2
m*m are the all-zero and identity matrices respectively. We shall refer to the structure of this
matrix as the M-companion structure. To study how to generate M companion matrix, article [38] explains the
algorithm with O (n4
) time complexity. In this article, we have used this paper to generate the configuration
matrix of σ−LFSR. The main purpose of σ−LFSR is to introduce a vector-based pseudorandom number
generator in our work. In this article, every operation is performed over Galois Field (GF (2)), ⊕ is used for
XOR between two integers, << sign is used for left shift operator, || is used for bitwise OR operator, ⊞ is used
for addition of two integers modulo 264 , F2
n
signifies n dimensional vector over GF(2), F2
n*n represents a matrix
of dimension n over GF(2) and F2
s Finite fields with 28
elements over F2.
PROPOSED APPROACHES
The Modified SNOW 3G algorithm comprises a σ− Linear Feedback Shift Register (LFSR) and nonlinear
Finite State Machine (FSM) used in SNOW 3G. The σ−LFSR has b = 8 delay blocks (Di |i ∈ [8]) of each is of
size m = 64 bit. Figure 1 describes the sketch of the SNOW 3G algorithm.

Fig. 1. Modified SNOW 3G
The LFSR part of Figure 1 has a feedback polynomial which has 8 gain matrices (Bi ∈ F2
64×64). The feedback polynomial x 8
+ B7x
7 + B6x
6 + · · · + B1x + B0 over matrix ring M64(F2) is generated from the primitive polynomial x512 + x419 + x321 + x125 + 1
over F2. In these contexts, we use the configuration matrix generation algorithm proposed by [38,39] to find the
feedback polynomial of the σ−LFSR. Next, we describe the driving equation of σ −LF SR and Finite State Machine (FSM).

In the above equation Di
t
is the value i−th delay block at tth timestamp and Ft
is output of an FSM at t
th time-stamp which
is described below. The FSM part of SNOW 3G consists of three registers R1
t
, R2
t
, R3
t ∈ F2
64 and two substitution boxes [6]
S1 and S2. We use 8 parallel S-BOXes (composed of AES Subbyte and Mixcolumn operation) to compute each S-BOX
function. Suppose bi
t
is the one-byte input data at t
th timestamp and bi
t+1 denotes the output data at t + 1 timestamp.
The general structure of the S-BOX equation 4 of S1, S2 as follows:

In equation 4 the matrix is circulant MDS[40] matrix where U ∈ F2
8 and generally U = 2 is chosen.
In equation 4, S(a) = 0 when a = 0, and S(a) = a
254 otherwise, where, a ∈ F2
8
.
The S-BOX equation can be written in the following:

where i ∈ {1, 2}, in ∈ F2
64and each inj ∈ F2
8
|j ∈ [8].
The registers R1, R2, R3 in the KSG are updated as follows:

where ⊞ is integer addition modulo 264 and ⊕ is vector wise XOR operation. 
