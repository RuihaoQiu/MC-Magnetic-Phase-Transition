This project is to use Markov Chain Monte Carlo method to simulate the behavior of spin orders in magnetic materials.

### Methods

**Monte Carlo Methods** are a broad class of computational algorithms that rely on repeated random sampling to obtain numerical results. Their essential idea is using random samples to solve problems that might be deterministic in principle. In physics-related problems, Monte Carlo methods are useful for simulating systems with many coupled degrees of freedom, for example, our spin interacting system. Here we introduce a specific Monte Carlo method — Markov Chain Monte Carlo (MCMC).

- Markov Chain Monte Carlo (MCMC) 

  Markov Chain is a dependent system, the next state of the system depends only on the present state.<br>
  All the probabilities are forming a transition matrix, each element in the matrix represents the possibility from one state to the other one. The Makov process will asymptotically reach a unique stationary distribution.<br>
  MCMC is simply to construct a Markov chain to do Monte Carlo approximation, the most used algorithm is Metropolis–Hastings Algorithm.

- Metropolis–Hastings Algorithm

  The Algorithm is illustrated as the pseudocode:<bt>
  1. Initialize a random state;<br>
  2. Pick up a random state according to the proposal distribution;<br>
  3. If satisfy the [Metropolis condition](https://en.wikipedia.org/wiki/Metropolis–Hastings_algorithm), the system transits to the new state; else, transition doesn't take place;<br>
  4. save the state, go to step 2.

The implemental details of MCMC in a magnetic lattice can be referred to<br>
[**MCMC implementation.ipynb**](https://nbviewer.jupyter.org/github/RuihaoQiu/MC-Magnetic-Phase-Transition/blob/master/MCMC-implementation.ipynb)

### Models

- **Mean-field Theory**

  For an individual particle in a many-body system, the effect from all the other particles is approximated by a single averaged effect, which reducing a many-body problem to a one-body problem.<br>
  We call it Mean-field Theory.<br>
  First, we use Mean-field Theory to estimate the Néel temperature of the magnetic system, please refer to (Attention, lots of formulas!!!)<br>
  [**Mean-field Theory.ipynb**](https://nbviewer.jupyter.org/github/RuihaoQiu/MC-Magnetic-Phase-Transition/blob/master/Mean-field-theory.ipynb)

- **Ising Model**

  - 2D Ising Model

    In 2D Ising model, the spins are lying in xy​-plane and oriented only along either +y​ or -y directions. The following figure shows the Monte Carlo process.

    <p align="center"><img src="data-and-images/2d_vector.gif" style="width: 60%; height: 50%"></p>

    The codes and other details are in the following page:<br>
    [**2D-Ising-model.ipynb**](https://nbviewer.jupyter.org/github/RuihaoQIU/MC-Magnetic-Phase-Transition/blob/master/2D-Ising-model.ipynb)

  - 3D Ising model

    In 3D Ising model, the spins are oriented to two directions, represent by red and blue dots in the following figure.

    <p align="center"><img src="data-and-images/3d_points.gif" style="width:80%; height:30%"></p>
    
    The codes and all the details are in file:<br>   
    [**3D-Ising-model.ipynb**](https://nbviewer.jupyter.org/github/RuihaoQIU/MC-Magnetic-Phase-Transition/blob/master/3D-Ising-model.ipynb)

- **3D Heisenberg Model**

  This model allow the spin change both direction and magnitude. The code is in the following file:<br>
  [**3D-Heisenberg Model.ipynb**](https://nbviewer.jupyter.org/github/RuihaoQIU/MC-Magnetic-Phase-Transition/blob/master/3D-Heisenberg-model.ipynb)

