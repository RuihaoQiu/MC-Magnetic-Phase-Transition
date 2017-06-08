# Monte Carlo Simulations on Magnetic Phase Transition.

This project is to use Monte Carlo method to simulate the behaviour of spins in magnetic materials.

### Methods

**Monte Carlo Methods** are a broad class of computational algorithms that rely on repeated random sampling to obtain numerical results. Their essential idea is using random samples to solve problems that might be deterministic in principle. In physics-related problems, Monte Carlo methods are useful for simulating systems with many coupled degrees of freedom, for example, our spin interacting system. Here we introduce a specific Monte Carlo method — Markov Chain Monte Carlo (MCMC).

- [Markov Chain Monte Carlo]() (MCMC) 

  Construct a Markov chain to do Monte Carlo approximation.

- [Metropolis–Hastings Algorithm]()

  The Algorithm is illustrated as the pseudocode:

  1. Initialize x(0)

  2. For i = 0 to N

     - Sample u ~ U(0, 1)

     - Sample x* ~ q(x*|x(i))

     - If u < A(x(i), x\*) = min{1, p(x\*)q(x(i)|x\*) / p(x(i))q(x\*|x(i))}

       ​	x(i+1) = x*

       else

       ​	x(i+1) = x(i)

### Models

- [**Mean-field Theory**]()

  For an individual particle in a many-body system, the effect from all the other particles is approximated by a single averaged effect, which reducing a many-body problem to a one-body problem.

  [Estimate Neél temperature by mean-field theory]()


- **Ising Model**

  [Theory](https://nbviewer.jupyter.org/github/RuihaoQIU/MC-Magnetic-Phase-Transition/blob/master/Ising-model-theory.ipynb)

  [2D Ising Model](https://nbviewer.jupyter.org/github/RuihaoQIU/MC-Magnetic-Phase-Transition/blob/master/2D-Ising-model.ipynb)

  [3D Ising Model](https://nbviewer.jupyter.org/github/RuihaoQIU/MC-Magnetic-Phase-Transition/blob/master/3D-Ising-model.ipynb)

- **Heisenberg Model**

  [Theory](https://nbviewer.jupyter.org/github/RuihaoQIU/MC-Magnetic-Phase-Transition/blob/master/Heisenberg-model.ipynb)

  [3D Heisenberg Model](https://nbviewer.jupyter.org/github/RuihaoQIU/MC-Magnetic-Phase-Transition/blob/master/MC-3D-Heisenberg-model.ipynb)

