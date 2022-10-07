---
title: "Magic state resource theory and quantum advantage"
mathjax: true
layout: page
syntax-id: footnotes
categories: media
permalink: "/magicprova/"
---


Quantum computers are more powerful than classical computer. They provide an overwhelming speed-up, the so-called quantum advantage, on certein computational tasks. Two quantum resources are responsible for the quantum advantage, magic and entanglement. It is a striking fact that these two resources can be hierercarized from the point of view of quantum complexity. Indeed, entanglement can be created by means of unitary operators belonging to a subgroup of the unitary group, the Clifford group. States created by the action of the Clifford group on computational basis states are called stabilizer states. This special class of states admits a efficient classical representation and, as a consequence, quantum computation emplying stabilizer states only can be efficiently reproduced by classical computers. Therefore, although these states are highly entangled, they lack computational power. To unlock quantum advantage one needs non-Clifford gates. 

On the other hand, quantum computation employing non-entangling and magic gates can still be efficiently simulated classically with an algorithm scaling linearly in the number of qubits. Such a simple consideration tells that is rather the conjuction of these two resources, magic and entanglement, that allows computation attaining advantage over classical computation. While the interplay between these two resources is not clear yet, in what follows, we will only focus to the framework for which the entanglement is a free resource, indeed created by entangling Clifford gates, while magic is the expensive one. 

States created by some non-Clifford gates are said to possess magic. Magic state resource theory has been widely employed for the problem of classical simulation of quantum dynamics. Clearly, quantum computation that can be efficiently reproduced classically cannot afford any quantum advantage. The question is: how many non-Clifford gates are, at least, necessary to achieve quantum advantage? An hint to this answer can be found in, where Bravyi and Gosset proved that the classical simulations of Clifford circuits doped with \\(t\\) non-Clifford gates is polynomially in the number of qubits \\(n\\), and exponential in \\(t\\). Thus, states created by, at least, \\(O(n)\\) non-Clifford gates can achieve a quantum speed-up. A measure of magic, say 
\\(M(|\psi\rangle)\\), should therefore have the operational meaning of non-classical simulability: the more \\(M(|\psi\rangle)\\) increases the more expensive is the classical simulation of \\(|\psi\rangle\\).

One of the first introduced measure of magic, the [robustness of magic](https://arxiv.org/abs/1609.07488)
\\(R(|\psi\rangle)\\), has exaclty this property: let \\(N\\) be the number of non-classical resources needed for the classical simulation of \\(|\psi\rangle\\), then:

$$ N=O(e^{R(|\psi\rangle)}) $$

Unfortutately, the robustness of magic involves a minimization procedure over all the stabilizer decomposition of \\(|\psi\rangle\\), which makes the computation of \\(R(|\psi\rangle)}\\) impossible even for \\(n\sim 5\\). We introduced a novel measure of magic in terms of an entropic quantity, the Stabilizer Rènyi entropy \\(M(|\psi\rangle)\\). We show that a family of magic measure is obtained by the Rènyi entropies of the probability distribution given by the expectation value of Pauli strings. Let \\(\mathbb{P}\\) the set of all Pauli string, then:

$$ \Xi(P):=\frac{\langle\psi|P|\psi\rangle^2}{d} $$

is a probability distribution, i.e. \\(\sum_{P\in\mathbb{P}}\Xi(P)=1\\). The stabilizer Rènyi entropy is defined as:

$$ M_{\alpha}(|\psi\rangle)= S_{\alpha}(\Xi)-\log d $$

where \\(S_{\alpha}(\Xi)\\) is the [\\(\alpha\\)-Rènyi entropy](https://en.wikipedia.org/wiki/Rényi_entropy) of the probability distribution \\(\Xi\\). The properties that make the Stabilizer Rènyi entropy an excellent candidate as a measure of magic are:



$$ M_{\alpha}(|\psi\rangle)\le 2 R(|\psi\rangle) $$

these three properties listed above allow a computation of the classical simulation overhead, \\(N\\) defined above, possible up to \\(n\sim 20\\). With the stabilizer Rènyi entropy we can readily reproduce the result from Bravyi and Gosset: let \\(t\\) be the number of non-Clifford gates used to create the state \\(|\psi\rangle_t\\), then:

$$ M(|\psi\rangle_t)\approx t$$

using the lower bound to the robustness of magic, the number of classical resources needed to classically simulate \\(|\psi\rangle_t\\) scale exponentially in \\(t\\). Thus, in the [NISQ](https://arxiv.org/abs/1801.00862) era, it is of paramount importance to be able to characterize the proposed hardware on how good these machines are at performing quantum computation to attain an advantage over classical computation. In a subsequent work^[1], we indeed experimentally measure the stabilizer R\`enyi entropy on two IBM quantum falcon processors and characterize their ability to create a reliable amount of magic. Below the first direct measurement of the magic possesses by single qubit states:

![experiment](experiment1.png)


However, one of the main features of the Stabilizer Rènyi entropy is that it is able to reveal the tight connection between the resource theory of magic and the concept of quantum chaos. The amount of magic that a unitary evolution can generate, its \textit{non-stabilizing power}, is intimately connected to multi-point OTOCs. In particular, the $k$-th R\`enyi entropy of the [Choi state](https://en.wikipedia.org/wiki/Choi–Jamiołkowski_isomorphism) \\(|U\rangle\\) associated with a unitary operator $U$ is equal to the logarithm of a $4k$-point OTOC associated with $U$:

$$ M_{\alpha}(|U\rangle)=\frac{1}{1-\alpha}\log \operatorname{OTOC}_{4\alpha}(U)$$

This simple equation allows speculations on the nature of quantum chaos and its relation with magic generation: only those unitaries with maximal non-stabilizing power can be considered chaotic. This constitutes a decisive step toward the comprehension of quantum chaos: the less simulable a quantum computation results, the more chaotic the quantum evolution, generated by that circuit, is. In particular, a given unitary operator attains the Haar value for the general $4k$ point OTOC - and thus it is considered chaotic according to the above definition - if and only if it can generate a maximal amount of magic with respect to the Stabilizer R\`enyi entropy of any order $k$. As a result, quantum chaotic evolutions are the ones able to unlock quantum advantage. 

[More on quantum chaos](https://lorenzoleone.github.io/quantumchaos/)






