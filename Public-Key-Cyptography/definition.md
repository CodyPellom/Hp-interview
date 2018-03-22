    Public Key Encryption System
In a public key encryption system, any person can encrypt a message using the receiver's public key. That encrypted message can only be decrypted with the receiver's private key. To be practical, the generation of a public and private key -pair must be computationally economical. The strength of a public key cryptography system relies on the computational effort (work factor in cryptography) required to find the private key from its paired public key. If so, effective security only requires keeping the private key private; the public key can be openly distributed without compromising security.

    Public key infrastructure

Public key infrastructures (PKIs) have been proposed as a way around this problem of identity authentication. In their most usual implementation, each user applies to a 'certificate authority' for a digital certificate which serves for other users as a non-tamperable authentication of identity, at the risk of compromising every user in case the CA itself is compromised.

Several countries and other jurisdictions have passed legislation or issued regulations encouraging PKIs by giving (more or less) legal effect to these digital certificates. Several commercial firms, and a few government departments, have established such certificate authorities. VeriSign is the most prominent commercial firm.

This does nothing to solve the problem though, as the trustworthiness of the CA itself is still not guaranteed for any particular individual. It is a form of argument from authority fallacy. For actual trustworthiness, personal verification that the certificate belongs to the CA and establishment of trust in the CA are required. This is usually not possible.

For those new to such things, these arrangements are best thought of as electronic notary endorsements that “this public key belongs to this user”. As with notary endorsements, there can be mistakes or misunderstandings in such vouchings. Additionally, the notary itself can be untrusted. There have been several high-profile public failures by assorted certificate authorities.[citation needed]

    Diffie–Hellman key exchange

In 1976, Whitfield Diffie and Martin Hellman published a cryptographic protocol called the Diffie–Hellman key exchange (D–H) based on concepts developed by Hellman's PhD student Ralph Merkle. The protocol enables users to securely exchange secret keys even if an opponent is monitoring that communication channel. The D–H key exchange protocol, however, does not by itself address authentication (i.e. the problem of being sure of the actual identity of the person or 'entity' at the other end of the communication channel). Authentication is crucial when an opponent can both monitor and alter messages within the communication channel (AKA man-in-the-middle or MITM attacks) and was addressed in the fourth section of the paper.

    Quantum Key Distribution
Quantum key distribution (QKD) is a secure communication method which implements a cryptographic protocol involving components of quantum mechanics. It enables two parties to produce a shared random secret key known only to them, which can then be used to encrypt and decrypt messages. It is often incorrectly called quantum cryptography, as it is the best-known example of a quantum cryptographic task.

An important and unique property of quantum key distribution is the ability of the two communicating users to detect the presence of any third party trying to gain knowledge of the key. This results from a fundamental aspect of quantum mechanics: the process of measuring a quantum system in general disturbs the system. A third party trying to eavesdrop on the key must in some way measure it, thus introducing detectable anomalies. By using quantum superpositions or quantum entanglement and transmitting information in quantum states, a communication system can be implemented that detects eavesdropping. If the level of eavesdropping is below a certain threshold, a key can be produced that is guaranteed to be secure (i.e. the eavesdropper has no information about it), otherwise no secure key is possible and communication is aborted.

The security of encryption that uses quantum key distribution relies on the foundations of quantum mechanics, in contrast to traditional public key cryptography, which relies on the computational difficulty of certain mathematical functions, and cannot provide any mathematical proof as to the actual complexity of reversing the one-way functions used. QKD has provable security based on information theory, and forward secrecy.

Quantum key distribution is only used to produce and distribute a key, not to transmit any message data. This key can then be used with any chosen encryption algorithm to encrypt (and decrypt) a message, which can then be transmitted over a standard communication channel. The algorithm most commonly associated with QKD is the one-time pad, as it is provably secure when used with a secret, random key.[1] In real-world situations, it is often also used with encryption using symmetric key algorithms like the Advanced Encryption Standard algorithm.

    Privacy amplification 

is a method for reducing (and effectively eliminating) Eve's partial information about Alice and Bob's key. This partial information could have been gained both by eavesdropping on the quantum channel during key transmission (thus introducing detectable errors), and on the public channel during information reconciliation (where it is assumed Eve gains all possible parity information). Privacy amplification uses Alice and Bob's key to produce a new, shorter key, in such a way that Eve has only negligible information about the new key. This can be done using a universal hash function, chosen at random from a publicly known set of such functions, which takes as its input a binary string of length equal to the key and outputs a binary string of a chosen shorter length. The amount by which this new key is shortened is calculated, based on how much information Eve could have gained about the old key (which is known due to the errors this would introduce), in order to reduce the probability of Eve having any knowledge of the new key to a very low value.

    Implementations


            Experimental
The highest bit rate system currently demonstrated exchanges secure keys at 1 Mbit/s (over 20 km of optical fibre) and 10 kbit/s (over 100 km of fibre), achieved by a collaboration between the University of Cambridge and Toshiba using the BB84 protocol with decoy state pulses.[9]

In 2007, Los Alamos National Laboratory/NIST achieved quantum key distribution over a 148.7 km of optic fibre using the BB84 protocol.[10] Significantly, this distance is long enough for almost all the spans found in today's fibre networks. A European collaboration achieved free space QKD over 144 km between two of the Canary Islands using entangled photons (the Ekert scheme) in 2006,[11] and using BB84 enhanced with decoy states[12][13] in 2007.[14]

As of August 2015 the longest distance for optical fiber (307 km)[15] was achieved by University of Geneva and Corning Inc. In the same experiment, a secret key rate of 12.7 kbit/s was generated, making it the highest bit rate system over distances of 100 km.

In June 2017, physicists led by Thomas Jennewein at the Institute for Quantum Computing and the University of Waterloo in Waterloo, Canada achieved the first demonstration of quantum key distribution from a ground transmitter to a moving aircraft. They reported optical links with distances between 3–10 km and generated secure keys up to 868 kilobytes in length.[16]

Also in June 2017, as part of the Quantum Experiments at Space Scale project, Chinese physicists led by Pan Jianwei at the University of Science and Technology of China measured entangled photons over a distance of 1203 km between two ground stations, laying the groundwork for future intercontinental quantum key distribution experiments.[17] Photons were sent from one ground station to the satellite they had named Micius and back down to another ground station, where they "observed a survival of two-photon entanglement and a violation of Bell inequality by 2.37 ± 0.09 under strict Einstein locality conditions" along a "summed length varying from 1600 to 2400 kilometers."[18]
