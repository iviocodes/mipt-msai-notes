# Vector Spaces

## 1. What is a Vector Space?

A **vector space** is a set where you can add things together and multiply them by numbers (“scalars”), and the results stay within the set. The rules are:
- **Addition**: If you have two vectors $\vec{u}, \vec{v}$, then $\vec{u} + \vec{v}$ is also a vector in that space.
- **Scalar multiplication**: Multiply a vector $\vec{v}$ by a number $a$ to get another vector: $a \vec{v}$.
- There are other properties (like distributivity, existence of a zero vector, etc.), but these are the core.

**Example:** The set of all ordered pairs of real numbers $(x, y)$ is a vector space: $\mathbb{R}^2$.

## 2. Hierarchy of Spaces

- **Vector Space**: Most general setting for linear algebra.
- **Normed Space**: A vector space with a way to measure “length” (norm).
- **Inner Product Space**: A normed space where you can take “dot products” (measuring angles).
- **Euclidean Space**: The example you know best—$\mathbb{R}^n$ with the usual dot product, forming our usual geometry.

A simple mnemonic: 
> “All Euclidean spaces are inner product spaces, all inner product spaces are normed spaces, all normed spaces are vector spaces—but not vice versa.”

## 3. Norm and Inner Product

- **Norm**: Given a vector $\vec{v}$, the norm $\|\vec{v}\|$ is its length: 
  - For $\mathbb{R}^n$, $\|\vec{v}\| = \sqrt{v_1^2 + v_2^2 + \ldots + v_n^2}$.
- **Inner Product** (a.k.a. “Dot Product”): Measures the “angle” and “length together” between two vectors: $\vec{u} \cdot \vec{v} = u_1v_1 + u_2v_2 + \ldots + u_nv_n$

This leads to the **norm**: $\|\vec{v}\| = \sqrt{\vec{v} \cdot \vec{v}}$.

## 4. Euclidean Spaces
- These are just $\mathbb{R}^n$, with our standard rules for addition, scaling, and dot product.
- **Geometry**: Distance between points, measuring angles, etc. are all linked to the inner product structure.

## 5. Subspaces

### What is a Subspace?
A **subspace** is a "smaller" vector space inside a bigger one. For example, a line or a plane through the origin inside $\mathbb{R}^3$.

### Three Key Criteria
A subset $W$ of a vector space $V$ is a **subspace** if:
1. **Zero Vector:** $\vec{0} \in W$.
2. **Closed Under Addition:** For any $\vec{u}, \vec{v} \in W$, the sum $\vec{u} + \vec{v} \in W$.
3. **Closed Under Scalar Multiplication:** For any $\vec{v} \in W$ and any scalar $a$, $a\vec{v} \in W$.

If you see a set that doesn’t satisfy these, it’s not a subspace.

### Quick Examples
- **Entire vector space** itself: Always a subspace.
- **Line through origin:** E.g., all multiples of $(1, 2)$ inside $\mathbb{R}^2$.
- **Plane through origin:** E.g., all $(x, y, 0)$ inside $\mathbb{R}^3$.
- **Set of solutions to a homogeneous linear equation:** Like $ax + by = 0$, forms a subspace.

### Not Subspaces (Counterexamples)
- **Line not through origin:** E.g., $(1, 2) + t(3, 4)$ for $t \in \mathbb{R}$, where $(1, 2)$ isn’t the origin — this fails the zero vector criterion.
- **Subset not closed under addition/scalar multiplication:** E.g., only vectors of length 1.

### Why Are Subspaces Important?
- They often describe **solution sets** to linear systems.
- They’re the backbone of **span**, **basis**, and **dimension** concepts.

