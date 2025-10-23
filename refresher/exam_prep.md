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

>A simple mnemonic: 
“All Euclidean spaces are inner product spaces, all inner product spaces are normed spaces, all normed spaces are vector spaces—but not vice versa.”

## 3. Norm and Inner Product

- **Norm**: Given a vector $\vec{v}$, the norm $\|\vec{v}\|$ is its length: 
  For $\mathbb{R}^n$, $\|\vec{v}\| = \sqrt{v_1^2 + v_2^2 + \ldots + v_n^2}$.
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



# Vector Geometry

## 1. Angles Between Vectors

The angle $\theta$ between two vectors $\vec{a}$ and $\vec{b}$ in $\mathbb{R}^n$ uses their dot product: 

$$\cos \theta = \frac{\vec{a} \cdot \vec{b}}{|\vec{a}|\,|\vec{b}|}$$

To find $\theta$: 

$$\theta = \cos^{-1}\left(\frac{\vec{a} \cdot \vec{b}}{|\vec{a}|\,|\vec{b}|}\right)$$

This formula answers: “How much do the vectors 'point in the same direction'?”

## 2. Vector & Scalar Projections

**Scalar projection** (also called "component") of $\vec{a}$ onto $\vec{b}$:

$$
\text{comp}_{\vec{b}} \vec{a} = \frac{\vec{a} \cdot \vec{b}}{|\vec{b}|}
$$

This is just a number; it tells "how much of $\vec{a}$ is in the direction of $\vec{b}$".

**Vector projection** puts the scalar projection in the direction of $\vec{b}$:

$$
\text{proj}_{\vec{b}} \vec{a} = \frac{\vec{a} \cdot \vec{b}}{|
\vec{b}|^2} \vec{b}
$$

Think of it as the **"shadow"** of $\vec{a}$ on $\vec{b}$.

## 3. Orthogonal Projections

>**Orthogonalization** is the process of transforming a set of vectors or features into a new set where each pair is independent or "perpendicular" to each other. This is achieved by creating vectors with a dot product of zero, making them mutually orthogonal, and is often done using methods like the Gram-Schmidt process. 

Suppose you want the projection onto a subspace (like a plane) that is defined by some vector $\vec{b}$. The vector projection $\text{proj}_{\vec{b}} \vec{a}$ is always **orthogonal** to the difference $\vec{a} - \text{proj}_{\vec{b}} \vec{a}$ (the part left over is perpendicular to $\vec{b}$).

**In a nutshell:**

- The **orthogonal projection** of $\vec{a}$ onto a line (or vector) is its vector projection.
- The part perpendicular to $\vec{b}$ is called the "orthogonal complement".

## 4. Normals

A **normal** to a surface (like a plane) is a vector perpendicular to that surface.

- For a plane defined by $Ax + By + Cz = D$, the vector $(A, B, C)$ is normal to the plane.
- Normals are important for defining hyperplanes, reflecting vectors, optimization, and computer graphics.

## 5. Hyperplanes

A **hyperplane** in $\mathbb{R}^n$ is a flat subset with dimension $n-1$.

- In 3D, a plane is a hyperplane.
- General equation: $a_1 x_1 + a_2 x_2 + ... + a_n x_n = d$.
- The normal vector is $(a_1, ..., a_n)$, showing what direction is "perpendicular" to the hyperplane.


