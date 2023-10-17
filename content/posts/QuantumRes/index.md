---
title: "Signals approach to quantum resistance"
date: 2023-10-17
draft: false
summary: "An article detailing how signal's new PQXDH post-quantum security protocol"
---

Companies, universities, and foundations have been tirelessly working towards inventing some semblance of post-quantum security. Recently, Signal, the encrypted messaging application, released an interesting paper on that topic. The paper introduced the "PQXDH" or "Post-Quantum Extended Diffie-Hellman" key agreement protocol.

The premise of the protocol is centered around post-quantum resistance, it is still not a quantum-resistant solution. The core issue that quantum computing poses to internet security lies with Shor's algorithm. This algorithm uses quantum bits and is capable of identifying prime factors - a task that is highly complex when using traditional computers and thus used for all internet encryption. Currently, Shor's algorithm requires a quantum computer with at least 1000 qubits to function. As of now, IBM has released a quantum computer with 434 qubits, with the number seeming to follow Moore's Law (exponential growth). This implies that in the very near future, all existing encryption, and by extension, the notion of private data/information, could be permanently eradicated.

In anticipation of this, some malicious actors are adopting a strategy known as "harvest now, decrypt later". These actors capture large volumes of encrypted data, typically banking details or state secrets, with the intention of decrypting the data once they have access to a 1000-qubit machine. This means that regardless of whatever post-quantum security measure arises in the future, their data is no longer their own.

Signal, a platform heavily used by individuals who value privacy and encryption, has come up with a countermeasure to these "harvest now, decrypt later" attacks. Their method involves supplementing the existing encryption algorithms with a peer-to-peer (P2P) temporary private key, which is used to rehash the message. This key is peer-validated and subsequently discarded after the message has been received.

This strategy provides a level of protection against quantum attacks for Signal users' information starting from now and a method for others to emulate. However, while this works for now, as this new field of computing keeps growing the world will have to completely rethink encryption in order to prepare for everything that is to come.