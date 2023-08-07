# Introduction

![alt Quantum Entanglement](https://github.com/MTC-India/quantum-computing/blob/main/quantum%20entanglement/Picture1.png)

What does the word entanglement mean to us? Ordinarily it signifies a rather difficult or complicated relationship with another entity. Quantum Entanglement, similarly, lives up to its name. Regarded as a strange and spooky phenomenon for multiple years, it left scientists in awe and confusion.

Quantum Entanglement is an unusual phenomenon that shows how states of two particles at any distance from one another remain correlated or entangled. Any small change in one of these particles, shall reflect in the other. Experiments on quantum entanglement were demonstrated using photons. This event, seemingly defying Einstein’s theory of Relativity, gave rise to a baffling question. Can information move faster than light?
What is superposition?

To understand quantum entanglement, we must have the understanding of superposition. Superposition is characterised by the unknown. It refers to a system that can exist in multiple states simultaneously at a given time. For instance if one flips a coin and grasps it in their palm without checking it, it could be either heads or tails right? This premise is acceptable, however we have no knowledge of which one it is. In that instant, it is both heads and tails.
When a system is in superposition, we can view their states as outcomes with certain probabilities based on their characteristics.
For instance, we put a dice in a closed opaque box and shake it around. We would now like to know which side is facing the lid of the box. We know that this system is in superposition(all six faces are facing the lid) and that all six faces could be facing the lid with a 1/6th probability.

Now that we’ve covered superposition let us move on to entanglement.

# Quantum Entanglement 

Quantum entanglement is a phenomenon in the realm of quantum mechanics that has for long dazed and confused the scientific community at large. The key principle claims that there is a peculiar connection between particular quantum particles even when they are spatially separated. This interpretation in a classical method would violate the basic laws of the individuality of a particle. This also seems to violate what Albert Einstein said, the transmission of information cannot occur at a rate which is faster than. the speed of light. Quantum entanglement involves a correlation between the properties of entangled particles, such as their spin, position, or polarisation. Remarkably, when two particles become entangled, the state of one particle instantaneously influences the state of the other, regardless of the distance separating them.

## Quantum Entanglement in Computing

The principle of quantum entanglement in the domain of computing can be seen in the behaviour of Qubits, which are the fundamental particle of Quantum computing, they perform akin to bits in regular computing. The Qubits exist in a superposition state of 0 AND 1 unlike the regular bits which have a classically determined state of 1 OR 0. The value of a Qubit can only be determined at the time of measurement at which its value appears in a probabilistic state depending on the superposition state. Although the intrinsic benefits of entangled states might not be apparent, they hold significant utility in the domain of computing. The following are upcoming domains that use the principle of quantum entanglement-

1. SuperDense Coding

2. Quantum teleportation

3. Quantum cryptography

We shall look into each of these in detail over the next parts.

# SuperDense Coding

Superdense coding uses the principle of quantum entanglement in order to efficiently conduct classical communication. We can convey two bits of classical nature from one “User” to another by the use of one Qubit by using the aforementioned principle. The use of these methods can be extrapolated to convey messages of larger sizes in an exponential way. The basic method involves setting two initial Qubits into superpositional states(Bell state in order to ensure maximal entanglement) and providing one to both the receiver and the sender. The sender can use appropriate methods to convert the Qubit received into a form that can be converted to the final message by using the reverse of the method used initially to put the Qubits into the superposition.
## Method-

First the Qubits are put into superposition by using the hadamard and the controlled Not(CNOT) gate.

The two superpositioned Qubits are sent to the sender and receiver.

The sender uses the Qubit received to convert it to an appropriate form for the message that they wish to send by using the Identity, Z Pauli and X pauli matrix as per required.

For a message of 00- Identity Matrix

For a message of 01-X Pauli Matrix

For a message of 10-Z Pauli Matrix

For a message of 11- XZ Pauli Matrix

Now, this message is sent to the receiver, who knows the states are in superposition and uses the inverse( the CNOT proceeded by the Hadamard gate) in order to obtain the message required.

![alt SuperDense](https://github.com/MTC-India/quantum-computing/blob/main/quantum%20entanglement/Picture2.jpg)<br>
### Advantages-

1. Increased Security- The final message can only be decoded with the Qubit which the receiver has which is in superposition with the Qubit in the message. Even if the message is intercepted in the channel, it is useless without the other Qubit to run it against. In the small scale example it is easy to think that we could run it against the inverse of the aforementioned Matrices, However when the message is of a larger size, we will be using a combination of these gates to get the message into a form that can be “decoded”. This prevents reverse engineering the message. Hence the security of the message transmitted is increased.

2. Decreased bandwidth required- A message of 2 classical bits is transmitted with 1 bit channels. This can be extrapolated to allow a larger message to be transmitted with smaller bandwidths. The bandwidth required for transmission is inversely proportional to the message size. The bandwidth represents the number of classical bits that can be transmitted per Qubit , and it remains constant regardless of the message size. The bandwidth is 2 per Qubit regardless of the size of the message.

# Quantum Teleportation

Quantum Teleportation uses the phenomenon of quantum entanglement to completely transfer a Quantum state from one location to another, without actually physically transmitting the system. Initially the receiver and the sender have a entangled pair of qubits, which is in a bell state to ensure maximal entanglement.

The sender performs a joint measurement of the state they wish to transmit with the Qubit that they have. This extracts two bits of information for communication to the receiver.Now the receiver performs required gates as based on the measurement taken by the sender.Now the Qubit which was initially with the receiver is converted to the State that was supposed to be “teleported”.

We can see that teleportation does not exactly take place but the disappearance of quantum state from the sender and the appearance of the quantum state at the receiver is compared to teleportation.

## Method-

The CNOT gate is then applied with the first qubit serving as control and the second qubit as target.In the next stage, the Hadamard gate is applied to the first qubit.The measurements are performed on qubits 1 and 2, and based on the results of measurements, denoted respectively as a and b, the controlled-X (CNOT) and controlled-Z gates are applied conditionally. This allows some PSI to be “teleported”.<br>

![alt Teleportation](https://github.com/MTC-India/quantum-computing/blob/main/quantum%20entanglement/Picture3.jpg)<br>

### Advantages-

1)Security- same reason as Superdense coding

2)Long distance quantum communication- since the entangled bits being used by the sender and the receiver remain in superposition even at extremely long distances, the quantum information can be transferred across long distances without being affected by noise or decoherence.

# Quantum Cryptography 

Quantum cryptography is a method that uses the principles of quantum mechanics to ensure the safe and secure communication between two “Users”. Confidentiality and integrity of data are ensured by using quantum physics. It uses the Heisenberg uncertainty principle, which states that the position and momentum of a quantum particle cannot be precisely measured simultaneously. This principle is the basis for the security of the transmission.The basic principle of cryptography involves the use of an encryption key which is held by the sender and the receiver.However rather than classical mathematical algorithms,which can be reverse engineered, the secure nature of the quantum cryptography is due to fundamental laws of nature.

## Method-

First the sender dispatches a stream of photons (light particles when light is considered to be matter) to the receiver.These are polarised in order to represent a particular 0 or 1.They may be vertically/horizontally/circularly polarised.

The receiver measures the polarisation of these photons using a predetermined basis. Since the measurement of a quantum state causes disturbances in the quantum state, the state of some of the photons are changed randomly.

Finally the receiver and the sender compare the subset of their keys bits to estimate the error rate due the measurement disturbances. The procedure is then repeated until enough matching bits are present to know that the communication line is secure.

![alt Cryptography](https://github.com/MTC-India/quantum-computing/blob/main/quantum%20entanglement/Picture4.png)<br>

### Advantages-

Detection of eavesdroppers- Since the measurement of the quantum states causes a disturbance, any eavesdropper would cause a disturbance which would be noticed at the receiver's end. The receiver would compare the error with the average error and notice an increase which would turn the channel off, preventing any eavesdropper.

Security-The use of quantum mechanics uses the laws of nature to ensure security. Security from quantum and classical attacks are observed. Classical algorithms for the same,like the RSA can be cracked by the shor's algorithm on a classical computer.

Long Distance key distribution- The QKD process (quantum key distribution) enables safe transfer of the key across long distances by implementing symmetric encryption patterns.

These methods are rather difficult to implement currently, on a large scale due to technological limitations. I have attached basic codes for the functions which perform the aforementioned tasks, assuming that a classical message is two bits and a quantum state is represented by 1 Qubit.

