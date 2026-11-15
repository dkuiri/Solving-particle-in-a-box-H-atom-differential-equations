# Computational Physics: Quantum Mechanics and Differential Equations

This repository contains Python implementations of several problems in computational physics, quantum mechanics, statistical mechanics and numerical methods.

The project explores how mathematical and physical problems can be solved numerically using Python and scientific computing libraries. It includes calculations of quantum mechanical energy spectra, numerical integration, ordinary differential equations, diffusion processes and thermodynamic properties.

## 1. Particle in a One-Dimensional Box

The first problem investigates the one-dimensional time-independent Schrödinger equation for a particle confined in an infinite potential well.

Inside the box, the potential is zero, and the Schrödinger equation is

$$-\frac{\hbar^2}{2m}
\frac{d^2\psi}{dx^2}=
E\psi.
$$

A finite-difference matrix representation is constructed to obtain the numerical eigenvalues and eigenvectors.

The numerical energy spectrum is compared with the analytical energy levels:

$$
E_n=
\frac{n^2\pi^2\hbar^2}{2mL^2}.
$$

The notebook also visualizes the ground-state probability density and higher excited states.

**Topics covered:**
- Matrix representation of the Hamiltonian
- Numerical diagonalization
- Eigenvalues and eigenvectors
- Probability density
- Comparison with analytical energy levels

## 2. Hydrogen Atom

The hydrogen atom problem is solved numerically using the radial Schrödinger equation.

The radial equation is written in terms of the reduced radial wavefunction $u(r)$:

$$ -\frac{\hbar^2}{2m} \frac{d^2u}{dr^2}
+
\left[
-\frac{e^2}{4\pi\epsilon_0r}
+
\frac{\hbar^2l(l+1)}{2mr^2}
\right]u =
Eu.
$$

The calculation uses a finite-difference discretization of the radial Hamiltonian and sparse matrix diagonalization to obtain the energy eigenvalues and eigenvectors.

The notebook considers the $l=0$ case and plots the probability distributions of the lowest energy states.

**Topics covered:**
- Radial Schrödinger equation
- Coulomb potential
- Angular momentum contribution
- Finite-difference discretization
- Sparse matrix diagonalization
- Hydrogen atom energy eigenstates

## 3. Numerical Integration

This section explores numerical methods for evaluating definite and improper integrals.

### Definite Integration

The integral of a polynomial function is evaluated using numerical quadrature:

$$
I=\int_0^2 x^3\,dx.
$$

Two approaches are demonstrated:

- Gaussian quadrature using `scipy.integrate.quad`
- Simpson's integration method

### Improper Integration

The notebook also evaluates the normalization integral of a Gaussian distribution:

$$
I=
\int_{-\infty}^{\infty}
\frac{1}{\sigma\sqrt{2\pi}}
\exp\left[
-\frac{(x-\mu)^2}{2\sigma^2}
\right]dx.
$$

### Double Integration

Numerical double integration is explored using both nested quadrature and the `dblquad` function from SciPy.

**Topics covered:**
- Definite integrals
- Improper integrals
- Gaussian integration
- Double integration
- Numerical quadrature
- Simpson's method

## 4. Ordinary Differential Equations

The notebook demonstrates numerical solutions of first-order and second-order differential equations.

### First-Order Differential Equation

An exponential decay process is described by

$$
\frac{dx}{dt}=-kx.
$$

The equation is solved using `scipy.integrate.odeint`, and the resulting decay curve is plotted as a function of time.

### Second-Order Differential Equation

The damped harmonic oscillator is described by

$$
\frac{d^2x}{dt^2}
+
\lambda\frac{dx}{dt}
+
kx=0.
$$

The second-order equation is converted into a system of coupled first-order equations and solved numerically.

The time evolution of the oscillator is then visualized.

**Topics covered:**
- First-order differential equations
- Exponential decay
- Coupled differential equations
- Damped harmonic oscillator
- Numerical time evolution

## 5. Diffusion Equation

Numerical solutions of one-dimensional and two-dimensional diffusion equations are explored.

### One-Dimensional Diffusion

The diffusion equation is

$$
\frac{\partial u}{\partial t} =
\frac{\partial^2u}{\partial x^2}.
$$

An initially localized Gaussian distribution is evolved numerically using a finite-difference approach.

The initial and later distributions are plotted to illustrate the spreading of the density.

### Two-Dimensional Diffusion

The two-dimensional diffusion equation is

$$
\frac{\partial u}{\partial t} =
\frac{\partial^2u}{\partial x^2}
+
\frac{\partial^2u}{\partial y^2}.
$$

A localized initial distribution is evolved on a two-dimensional grid. The resulting distribution is visualized using a three-dimensional surface plot.

**Topics covered:**
- Diffusion equations
- Finite-difference methods
- Time evolution
- One-dimensional diffusion
- Two-dimensional diffusion
- Three-dimensional visualization

## 6. Statistical Mechanics

The final section explores a simple two-particle system in thermal equilibrium with a heat reservoir.

Each particle can occupy one of two energy levels, $0$ and $\epsilon$. The system is considered using Maxwell-Boltzmann statistics.

The notebook investigates several thermodynamic quantities.

### Partition Function

The partition function is expressed in terms of the energy levels and temperature.

### Average Energy

The average energy is calculated using

$$
\langle E\rangle =
\frac{
\sum_i g_i E_i
\exp(-E_i/k_BT)
}{Z}.
$$

### Energy Fluctuations

The relative root-mean-square energy fluctuation is evaluated numerically.

### Specific Heat

The temperature dependence of the specific heat is calculated using energy fluctuations:

$$
C_V=
\frac{
\langle E^2\rangle-\langle E\rangle^2
}{k_BT^2}.
$$

The results are plotted as functions of energy and temperature.

**Topics covered:**
- Maxwell-Boltzmann statistics
- Partition function
- Average energy
- Energy fluctuations
- Specific heat
- Temperature dependence of thermodynamic quantities

## 7. Repository Contents

| File | Description |
|---|---|
| `python_project.ipynb` | Main Jupyter notebook containing all numerical calculations and visualizations |

## 8. Software and Requirements

The project uses Python and the following scientific computing libraries:

- NumPy
- SciPy
- Matplotlib
- Jupyter Notebook
- IPyWidgets

## 9. Running the Notebook

Clone the repository:

```bash
git clone https://github.com/dkuiri/Solving-particle-in-a-box-H-atom-differential-equations.git
```

Navigate to the project directory:

```bash
cd Solving-particle-in-a-box-H-atom-differential-equations
```

Install the required packages:

```bash
pip install numpy scipy matplotlib jupyter ipywidgets
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open `python_project.ipynb` to explore the calculations and reproduce the numerical results.

## Author

**Dibyendu Kuiri**

Theoretical Condensed Matter Physics

[Personal Website](https://dkuiri.github.io/) | [Google Scholar](https://scholar.google.com/citations?user=K1jTqmYAAAAJ) | [LinkedIn](https://www.linkedin.com/in/dkuiri) | [GitHub](https://github.com/dkuiri)
