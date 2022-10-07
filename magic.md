---
title: "Magic state resource theory and quantum advantage"
mathjax: true
layout: page
categories: media
permalink: "/magic/"
---


Quantum computers are more powerful than classical computer. They provide an overwhelming speed-up, the so-called quantum advantage, on certein computational tasks. Two quantum resources are responsible for the quantum advantage, magic and entanglement. It is a striking fact that these two resources can be hierercarized from the point of view of quantum complexity. Indeed, entanglement can be created by means of unitary operators belonging to a subgroup of the unitary group, the Clifford group. States created by the action of the Clifford group on computational basis states are called stabilizer states. This special class of states admits a efficient classical representation and, as a consequence, quantum computation emplying stabilizer states only can be efficiently reproduced by classical computers. Therefore, although these states are highly entangled, they lack computational power. To unlock quantum advantage one needs non-Clifford gates. 

On the other hand, quantum computation employing non-entangling and magic gates can still be efficiently simulated classically with an algorithm scaling linearly in the number of qubits. Such a simple consideration tells that is rather the conjuction of these two resources, magic and entanglement, that allows computation attaining advantage over classical computation. While the interplay between these two resources is not clear yet, in what follows, we will only focus to the framework for which the entanglement is a free resource, indeed created by entangling Clifford gates, while magic is the expensive one. 

States created by some non-Clifford gates are said to possess magic. Magic state resource theory has been widely employed for the problem of classical simulation of quantum dynamics. Clearly, quantum computation that can be efficiently reproduced classically cannot afford any quantum advantage. The question is: how many non-Clifford gates are, at least, necessary to achieve quantum advantage? An hint to this answer can be found in, where Bravyi and Gosset proved that the classical simulations of Clifford circuits doped with \\(t\\) non-Clifford gates is polynomially in the number of qubits \\(n\\), and exponential in \\(t\\). Thus, states created by, at least, \\(O(n)\\) non-Clifford gates can achieve a quantum speed-up. A measure of magic, say \\(M(|\psi\rangle)\\), should therefore have the operational meaning of non-classical simulability: the more \\(M(|\psi\rangle)\\) increases the more expensive is the classical simulation of \\(|\psi\rangle\\).

One of the first introduced measure of magic, the [robustness of magic](https://arxiv.org/abs/1609.07488) \\(R(|\psi\rangle)\\), has exaclty this property: let \\(N\\) be the number of non-classical resources needed for the classical simulation of \\(|\psi\rangle\\), then:

$$ N=O(\exp(R(|\psi\rangle))) $$

We introduced a novel measure of magic in terms of an entropic quantity, the Stabilizer Rènyi entropy. We show that a family of magic measure is obtained by the Rènyi entropies of the probability distribution given by the expectation value of Pauli strings. Let \\(\mathbb{P}\\) the set of all Pauli string, then:

$$ \Xi(P):=\frac{\langle\psi|P|\psi\rangle^2}{d} $$

is a probability distribution, i.e. \\(\sum_{P\in\mathbb{P}}\Xi(P)=1\\). How does the magic scale with the number \\(t\\) of non-Clifford gates injected in the circuits? 


