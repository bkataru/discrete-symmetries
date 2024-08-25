---
marp: true
theme: default
_class: invert
paginate: true
---

# Discrete Symmetries of Quantum Field Theory



Baalateja Kataru

---

# Discrete Transformations

We'll take a look at the definition, properties, eigenvalues, and action on quantum fields of:

- Charge conjugation
  - Changes all particles $\ket{p}$ into their antiparticles $\ket{\bar{p}}$
- Parity reversal
  - Inverts the polarity of the spatial coordinates $(x, y, z) \mapsto (-x, -y, -z)$
- Time reversal
  - Reverses the flow of time by inverting the polarity of the temporal coordinate $t \mapsto -t$

Then, we'll investigate combining these discrete transformations to obtain certain **discrete symmetries** such as PT and CPT

---

# Charge conjugation

## Definition

- Changes all particles into their antiparticles and vice-versa
- Flips electromagnetic charge as well as other **quantum charges**
  - baryon number
  - lepton number
  - weak hypercharge
- Represented by the $\mathsf{C}$ operator

$$ \mathsf{C}\ket{p} = \ket{\bar{p}}$$

---

Suppose $p$ has charge $q$, which can be measured by a charge operator $\hat{Q}$

$$\hat{Q}\ket{p} = q\ket{p}$$

Similarly for $\ket{\bar{p}}$,

$$\hat{Q}\ket{\bar{p}} = -q\ket{\bar{p}}$$

Therefore,

$$\mathsf{C} \hat{Q} \ket{p} = q \mathsf{C} \ket{p} = q \ket{\hat{p}}$$

$$\hat{Q} \mathsf{C} \ket{p} = \hat{Q} \ket{\bar{p}} = -q \ket{\bar{p}}$$

---

Which implies that

$$\hat{Q} \mathsf{C} = -\mathsf{C} \hat{Q}$$

Or in other words,

$$\{ \hat{Q}, \mathsf{C} \} = 0$$

$$\mathsf{C}^{-1} \hat{Q} \mathsf{C} = - \hat{Q}$$

---

## Properties

Since

$$ \mathsf{C} \ket{p} = \ket{\bar{p}} $$

By normalization,

$$1 = \braket{p | p} = \braket{\bar{p} | \bar{p}} = \braket{p | \mathsf{C}^\dagger \mathsf{C} | p}$$

Therefore, $\mathsf{C}$ is **unitary**

$$\mathsf{C}^\dagger \mathsf{C} = 1$$

$$\mathsf{C}^\dagger = \mathsf{C}^{-1}$$

Now consider applying $\mathsf{C}$ twice,

$$\mathsf{C}^2 \ket{p} = \mathsf{C} \ket{\bar{p}} = \ket{p}$$

This implies that $\mathsf{C}$ is also **involutory**, i.e., it is its own inverse

$$\mathsf{C}^2 = 1 \implies \mathsf{C} = \mathsf{C}^{-1}$$

---

Putting all of this together,

$$\mathsf{C}^\dagger = \mathsf{C}^{-1}$$

$$\mathsf{C} = \mathsf{C}^{-1}$$

This implies that $\mathsf{C}$ is a **Hermitian** operator, i.e., it is an observable quantity with _real_ eigenvalues.

$$\mathsf{C} = \mathsf{C}^\dagger$$

---

## Eigenvalues

- Because $\mathsf{C}$ is both Hermitian and Unitary, its eigenvalues are real numbers of modulus unity, i.e. $\pm 1$
- Most particles are not eigenvalues of $C$ since if they were,

$$\mathsf{C}\ket{p} = \ket{\bar{p}} = \pm \ket{p} $$

- Which means that $\ket{p}$ is the same state as $\ket{\bar{p}}$, making the particle its own antiparticle. 
- This is true in some cases, esp. for particles with no quantum charges, but also for those with quantum charges such as Majorana fermions.
- Eg.: photon ($\gamma$) is an eigenstate of $\mathsf{C}$ with eigenvalue -1 since if you change all particles to their antiparticles, the electromagnetic field reverses $A^\mu \mapsto -A^\mu$
- Similarly, a neutral pion $\pi^0$ has an eigenvalue of +1 under $\mathsf{C}$. Hence, $\pi^0 \mapsto \gamma + \gamma$ is allowed because $+1 \mapsto (-1) \times (-1)$ matches up in terms of eigenvalues, but $\pi^0 \mapsto \gamma + \gamma + \gamma$ is not allowed.

---

## Field Transformation

For a complex scalar field (a real scalar field's particle is its own antiparticle), the mode expansions for the field operators are given as

$$\hat{\psi} = \int_{\textbf{p}} (\hat{a}_{\textbf{p}} e^{-i p \cdot x} + \hat{b}^{\dagger}_{\textbf{p}} e^{i p \cdot x})$$

$$\hat{\psi}^{\dagger} = \int_{\textbf{p}} (\hat{a}^{\dagger}_{\textbf{p}} e^{i p \cdot x} + \hat{b}_{\textbf{p}} e^{-i p \cdot x})$$

or more explicitly,

$$\begin{array}{rcl}\hat{\psi}(x) & = & \int\frac{\mathrm{d}^3p}{(2\pi)^{\frac32}}\frac1{(2E_{\boldsymbol{p}})^{\frac12}}\left(\hat{a}_{{p}}\mathrm{e}^{-\mathrm{i}p\cdot x}+\hat{b}_{{p}}^{\dagger}\mathrm{e}^{\mathrm{i}p\cdot x}\right),\\ \hat{\psi}^{\dagger}(x) & = & \int\frac{\mathrm{d}^3p}{(2\pi)^{\frac32}}\frac1{(2E_{\boldsymbol{p}})^{\frac12}}\left(\hat{a}_{{p}}^{\dagger}\mathrm{e}^{\mathrm{i}p\cdot x}+\hat{b}_{{p}}\mathrm{e}^{-\mathrm{i}p\cdot x}\right),\end{array}$$

---

Where 
- $\hat{a}^{\dagger}_p$ and $\hat{a}_p$ are the creation and annihilation operators for a particle with momentum $p$
- $\hat{b}^{\dagger}_p$ and $\hat{b}_p$ are the creation and annihilation operators for an antiparticle with momentum $p$

Therefore, for $\mathsf{C}$ to exchange particles and antiparticles, we must have that

$$\mathsf{C}^{-1}\hat{a}_{{p}}\mathsf{C}=\hat{b}_{{p}}$$

$$\mathsf{C}^{-1}\hat{b}_{\boldsymbol{p}}^\dagger\mathsf{C}=\hat{a}_{\boldsymbol{p}}^\dagger $$

(Note that $\mathsf{C}^\dagger = C$)

---

Then, for a complex scalar field $\hat{\psi}(x)$,

$$\begin{align}

\mathsf{C}^{-1} \hat{\psi} \mathsf{C} &= \int_{\textbf{p}} \mathsf{C}^{-1} (\hat{a}_{\textbf{p}} e^{-i p \cdot x} + \hat{b}^{\dagger}_{\textbf{p}} e^{i p \cdot x}) \mathsf{C} \\

&= \int_{\textbf{p}} (\hat{b}_{\textbf{p}} e^{-i p \cdot x} + \hat{a}^{\dagger}_{\textbf{p}} e^{i p \cdot x}) \\

\therefore \mathsf{C}^{-1} \hat{\psi} \mathsf{C} &= \hat{\psi}^\dagger

\end{align}$$

---

# Parity Inversion

## Definition

- Inverts the polarity of the spatial coordinates $(x, y, z) \mapsto (-x, -y, -z)$
- Notably has no effect on scalars and pseudovectors.
- Corresponds to a mirroring operation followed by a $180^\circ$ rotation about an axis perpendicular to the mirroring axis
- This transformation can be performed by the parity operator $\mathsf{P}$, which inverts the parity of the spatial coordinates $\textbf{x} \mapsto -\textbf{x}$. This means that the position operator will anticommute with $\mathsf{P}$

$$\hat{x}\mathsf{P} = - \mathsf{P} \hat{x}$$

$$\therefore \mathsf{P}^{-1} \hat{x} \mathsf{P} = - \hat{x}$$

---

## Properties

The effect on momentum coordinates is also the same $\textbf{p} \mapsto -\textbf{p}$, so

$$\mathsf{P}^{-1}\hat{\boldsymbol{p}}\mathsf{P}=-\hat{\boldsymbol{p}}$$

However, the canonical commutation relation $[\hat{x},\hat{p}_x]=\mathrm{i}$ will be preserved.

Since $P$ is **Hermitian**, i.e.,

$$\mathsf{P}^\dagger = \mathsf{P}$$

and since it is its own inverse (two inversions returns us to the same place again so $P$ is **involutory**)

$$P^2 = 1$$

Therefore, $P$ is also **unitary**

---

- The parity operation has no effect on scalars
- However, it reverses vectors.
- This is not completely true due to **pseudoscalars** and **pseudovectors**.
- **pseudoscalar**: a scalar formed via a scalar triple product.
- **pseudovector**: also called an **axial vector**, is formed by a cross product between two ordinary vectors (called **polar vectors**)

---

## Eigenvalues

---

## Field Transformation


---

# Time Reversal

## Definition
- Reverses the flow of time by inverting the polarity of the temporal coordinate $t \mapsto -t$

# PT symmetry



# CPT symmetry