# TNA Core Language v2.1: The Structural Grammar of Axiomatic Necessity

### Abstract

The Theory of Axiomatic Necessity (TNA) establishes a structural language describing the relationship between possibility, formal description, and instantiated realization. This version refines the original formulation by replacing the previously ambiguous notion of *Collapse* with two logically independent operators: *Projection* and *Coherence Restriction*. It further formalizes Coherence Restriction through explicit logical constraints, clarifies the relationship between the metatheoretic reading function and the core grammar, and specifies the exact locus of non-derivability in the operator chain.

## 1. Primitive Domains

TNA distinguishes three primitive domains:

### 1.1 Unlimited Structural Possibility ($N_{\infty}$)

The set of all structurally coherent possibilities. No temporal evolution is implied. No physical process is implied. It represents only logical possibility.
$$
N_{\infty} = \{S : S \text{ is a finite structural description}\}
$$
### 1.2 Descriptive Domain ($N_0$)

The domain of complete formal descriptions. Objects in $N_0$ consist of axiomatic systems, algorithms, mathematical structures, symbolic representations, and physical theories. Everything inside $N_0$ is describable. Nothing in its definition guarantees realizability.
$$
N_0 = \{s \in \mathcal{S} : s \text{ satisfies coherence constraints } C\}
$$
Where $\mathcal{S}$ is the set of projected structures and $C$ is defined below.

### 1.3 Instantiated Domain ($N_1$)

The domain of realized systems. Execution. Embodiment. Experience. Physical realization. Whatever ontology one adopts, realization belongs here rather than in $N_0$.
$$
N_1 = \{\sigma : \sigma \text{ is an instantiated realization of some } S \in N_0\}
$$

## 2. Structural Operators

TNA contains three primitive operators.

### 2.1 Projection ($P$)

$$
P : N_{\infty} \longrightarrow \mathcal{S}
$$

Projection extracts candidate finite structures from unlimited structural possibility. Projection is not selection. It merely identifies possible finite descriptions. The intermediate set $\mathcal{S}$ contains projected structures that are not yet guaranteed to be coherent:
$$
\mathcal{S} = \{s : \exists S \in N_{\infty}, s = P(S)\}
$$

### 2.2 Coherence Restriction ($R$)

$$
R : \mathcal{S} \longrightarrow N_0
$$

Coherence Restriction admits only structures satisfying explicit logical constraints.

**Definition 2.2.1 (Coherence Constraints $C$):** A structure $s \in \mathcal{S}$ satisfies $C$ if and only if:

- **Logical Consistency:** $s$ contains no contradictions derivable within its own inference rules:

  $$\nexists \phi : s \vdash \phi \land \neg \phi$$

- **Structural Completeness:** $s$ has a well-defined model (possibly empty):

  $$\exists M : M \models s$$

- **Compactness:** Every finite subset of $s$ is satisfiable:

  $$\forall s' \subseteq_{\text{fin}} s, \exists M' : M' \models s'$$

Then:
$$
R(s) = \begin{cases} s & \text{if } s \in C \\ \text{undefined} & \text{otherwise} \end{cases}
$$
And consequently:
$$
N_0 = R(\mathcal{S}) = \{R(s) : s \in \mathcal{S}, s \in C\}
$$
*Note: The previous term "Collapse" referred simultaneously to P and R. This generated the misleading impression that TNA proposed a physical collapse analogous to interpretations of quantum mechanics. Version 2 removes this ambiguity.*

### 2.3 Instantiation ($I$)

$$
I : N_0 \longrightarrow N_1
$$

Instantiation transforms a complete description into a realized system.

Importantly, TNA deliberately leaves $I$ undefined. Its interpretation depends upon the ontology under consideration. Examples include biological realization, phenomenological experience, physical execution, quantum consciousness, and computational implementation. TNA specifies only that instantiation is structurally distinct from description.

## 3. Exteriority

The Theorem of Axiomatic Necessity proves that every coherent formal system possesses indispensable structural elements that cannot be internally eliminated.

**Theorem 3.1 (Axiomatic Necessity):** For every $S \in N_0$, there exists a minimal finite set $A_{\text{min}}(S) \subseteq S$ such that:

1. $S$ is coherent $\iff A_{\text{min}}(S)$ is coherent.
2. $\forall a \in A_{\text{min}}(S), S \setminus \{a\}$ is not coherent.

Exteriority therefore represents a logical property of coherent systems. It is neither spatial nor temporal.

## 4. Structural Non-Derivability Corollary

Introducing the distinction between description and realization yields:

**Corollary 4.1 (Structural Non-Derivability):** Let $S \in N_0$ be a complete formal description, and $\sigma \in N_1$ its realization. Then:
$$
N_0 \not\vdash I
$$
No complete description derives its own instantiation operator.

### Locus of Non-Derivability

The non-derivability occurs specifically at the Instantiation operator $I$, not at $P$ or $R$:

| **Operator**                                 | **Computability Status**                    | **Nature**                    |
| -------------------------------------------- | ------------------------------------------- | ----------------------------- |
| $P : N_{\infty} \longrightarrow \mathcal{S}$ | Computable (selection of finite structures) | Formal operation              |
| $R : \mathcal{S} \longrightarrow N_0$        | Computable (consistency check)              | Formal operation              |
| $I : N_0 \longrightarrow N_1$                | Not computable within $N_0$                 | **Locus of non-derivability** |

#### Proof Sketch:

Suppose $I$ were computable within $N_0$. Then there would exist an effective procedure $\Pi_I \subseteq N_0$ such that for any $S \in N_0$, $\Pi_I(S) = \sigma \in N_1$.

But $I(S) = \sigma$ requires that $\sigma$ be recognized as the realized instantiation of $S$, not merely another description. The recognition of realization requires a criterion of admissibility that is not contained in $S$ itself (by Theorem 3.1).

Therefore, $\Pi_I$ would need to contain its own admissibility condition, generating the same regress identified in the general TNA irreducibility theorem:
$$
\Pi_I^{(1)} \longleftarrow \Pi_I^{(2)} \longleftarrow \Pi_I^{(3)} \longleftarrow \cdots
$$
Hence:
$$
I \not\subseteq N_0
$$
*Note: This statement is independent of the ontology adopted for $N_1$.*

## 5. Structural Grammar

The complete grammar of TNA becomes:
$$
N_{\infty} \xrightarrow{\quad P \quad} \mathcal{S} \xrightarrow{\quad R \quad} N_0 \xrightarrow{\quad I \quad} N_1
$$
Where:

- $P$ generates candidate finite structures.
- $R$ preserves only coherent structures.
- $I$ realizes descriptive structures.

The fundamental structural invariant remains:
$$
N_0 \not\vdash N_1
$$

## 6. Semantic Neutrality

The operators $P, R, I$ are purely structural. TNA itself commits to none of these ontological interpretations:

| **Theory / Paradigm**       | **Interpretation of N1**    |
| --------------------------- | --------------------------- |
| **Physicalism**             | Physical realization        |
| **Quantum Information**     | Quantum state actualization |
| **Panpsychism**             | Conscious realization       |
| **Phenomenology**           | Lived experience            |
| **Artificial Intelligence** | Computational execution     |
| **Process Philosophy**      | Becoming                    |

## 7. Structural Invariants

Once translated into TNA, many apparently unrelated theories become structurally identical:

| **Domain**         | **N0**                | **N1**                 | **Invariant Expression**                                    |
| ------------------ | --------------------- | ---------------------- | ----------------------------------------------------------- |
| **Gödel**          | Formal system $F$     | Metamathematical truth | $$F \not\vdash \text{Con}(F)$$                              |
| **Mary (Jackson)** | Physical knowledge    | Experience of red      | $$\Sigma_{\text{phys}} \not\vdash \sigma_{\text{exp}}^{*}$$ |
| **Batty**          | Design specifications | Self-awareness         | $$\text{Design} \not\vdash \text{consciousness}$$           |
| **Software Gap**   | Brain structure       | Culture/Symbolic Order | $$\text{Biology} \not\vdash \text{civilization}$$           |
| **Hawking-Lennox** | Physical laws         | Universe existence     | $$\text{Laws} \not\vdash \text{instantiation}$$             |

The semantics differ. The grammar remains invariant:
$$
N_0 \not\vdash N_1
$$

## 8. Conclusion

Version 2.1 clarifies that TNA contains no physical collapse mechanism. Its formalism consists of three structural operators $P, R, I$ acting over the structural domains $N_{\infty}, \mathcal{S}, N_0, N_1$.

The Theory of Axiomatic Necessity therefore becomes a genuine structural calculus rather than a collection of philosophical principles. The central invariant remains:
$$
N_0 \not\vdash N_1
$$
Which expresses the irreducibility of instantiated realization to complete formal description, independently of the ontology chosen to interpret the formalism.

## Appendix A: On the Reading Function

The reading function $L$ introduced in previous versions is a metatheoretic construct, not part of the core grammar.

**Definition A.1 (Reading Function):** Let $\mathcal{C}$ be a configuration space with internal dynamics $\mathcal{R} \subseteq \mathcal{C} \times \mathcal{C}$. A reading function is defined as:

$$L : \mathcal{C} \longrightarrow \mathcal{D}$$

Where $\mathcal{D}$ is a reduced semantic space.

### Relationship to Core Grammar

| **Metatheory**                                         | **Core Grammar**                                        |
| ------------------------------------------------------ | ------------------------------------------------------- |
| $\mathcal{C}$                                          | $N_{\infty}$ (unlimited possibility)                    |
| $\mathcal{D}$                                          | $N_0$ (descriptive domain)                              |
| $\mathcal{R} \subseteq \mathcal{C} \times \mathcal{C}$ | Dynamics of projection $P$                              |
| $L$                                                    | The observer's descriptive act (not an operator of TNA) |

The reading function $L$ explains why "collapse" appears in natural language descriptions of TNA: $L$ is typically non-injective, creating the illusion of state reduction where only structural reconfiguration occurs.

*Important: $L$ is not part of the formalism. It is a tool for analyzing how the formalism is interpreted.*

## Appendix B: Counterexamples and Boundary Cases

### B.1 — Local Injectivity of the Reading Function

If $L$ is injective over $\mathcal{C}' \subseteq \mathcal{C}$, then no interpretative collapse occurs within that restricted domain.

### B.2 — Semantic Degeneracy Without Structural Dynamics

Multiple structurally distinct states may be indistinguishable in $\mathcal{D}$ without any dynamic transition justifying selection. Collapse is purely epistemic.

### B.3 — Internal Symmetries

If $\mathcal{C}$ possesses symmetries $\mathcal{S}_y$ such that distinct configurations are equivalent under $\mathcal{S}_y$, apparent information loss reflects structural redundancy.

### B.4 — Semantic Granularity Limit

When the resolution of $\mathcal{D}$ is insufficient to distinguish states in $\mathcal{C}$, "collapse" is an artifact of coarse-graining.

## References

- Bresciano, C. (2025). *Theory of Axiomatic Necessity: Foundations and Closure Theorem*. Zenodo. DOI: 10.5281/zenodo.18098558.
- Bresciano, C. (2026). *Failure of Local Closure in Self-Optimizing Systems*. Zenodo. DOI: 10.5281/zenodo.18644522.
- Bresciano, C. (2026). *Boundary Conditions as Structural Selectors*. Zenodo. DOI: 10.5281/zenodo.20479474.
- Bresciano, C. (2026). *Castello Aereo Non Stat*. Zenodo. DOI: 10.5281/zenodo.20597938.
