+++
title = "Thomas Chaffey"
hascode = true
date = Date(2023, 08, 22)
rss = "Research in nonlinear control systems, circuits and optimization."
+++
@def tags = ["control", "research", "circuits", "optimization"]

# Research interests
Much of my work involves revisiting classical nonlinear input/output systems theory
and nonlinear circuit theory with modern methods from optimization.  Particular interests include:

* graphical analysis and design methods
* monotone operator methods in large-scale optimization
* the interplay between circuit theory and convex optimization
* analogue neuromorphic circuits
* behavioural models of systems

I love searching for connections between the latest research topics and old, forgotten ideas.  My two biggest heros are probably [Jan Willems](https://homes.esat.kuleuven.be/~sistawww/smc/jwillems/) and [George Zames](http://www.mit.edu/~mitter/publications/85_legacy_zames_IEEEAC.pdf).

# Bio
I am currently a Research Fellow at [Pembroke College, Cambridge](https://www.pem.cam.ac.uk/college/master-and-fellows/list-fellows/dr-tom-chaffey).  I completed my PhD in April 2022 in the Control Group, University of Cambridge, supervised by [Rodolphe Sepulchre](https://sites.google.com/site/rsepulchre/).  From August 2022, I spent seven weeks as a visiting researcher in the Department of Automatic Control at Lund University, Sweden.  My undergraduate degree was in mathematics and computer science, and my masters was in mechanical engineering, both at the University of Sydney, Australia.  I'm a qualified welder, and I love rock climbing, cycling, surfing and music (especially Bach and anything with a time signature of 7).

In 2023 I was interviewed for the [IEEE Control Systems "PhDs in Control" column](https://ieeexplore.ieee.org/document/10015605).

# Publications
For a full list of publications, see my [Google Scholar page](https://scholar.google.nl/citations?user=mpR3WKgAAAAJ&hl=en).  A copy of my PhD thesis can be downloaded [here](/assets/pdf/Tom_thesis.pdf).  Please let me know if you find any typos.

# Projects

## Scaled Relative Graphs for system analysis

@@im-50
![SRG](/assets/images/srg.svg)
@@
Scaled Relative Graphs (SRGs) are a new tool in optimization, developed by [Ernest Ryu, Robert Hannah and Wotao Yin](https://link.springer.com/article/10.1007/s10107-021-01639-w) for the study of convergence of optimization algorithms.  My project studies the relationship between the SRG and the classical Nyquist diagram of LTI control theory.  

The SRG is a generalization of the Nyquist diagram to stable nonlinear operators.  Like the Nyquist diagram, the SRG can be used to determine when a feedback system will be stable.  Studying stability with SRGs gives a graphical unification of many existing results on incremental stability, and opens up an entirely new avenue for studying nonlinear system properties.  Particularly interesting properties include nonlinear robustness margins defined as distances between SRGs.  

The figure above shows an analytical SRG of an LTI transfer function (left, Nyquist diagram in black), and a sampling of the SRG of Hodgkin and Huxley's potassium conductance (right).

### Publications
* Chaffey, Forni, Sepulchre, *Graphical Nonlinear System Analysis*, IEEE Transactions on Automatic Control, 2023 (early access), [journal](https://ieeexplore.ieee.org/document/10005799), [arxiv](https://arxiv.org/abs/2107.11272)
* Chaffey, *A rolled-off passivity theorem*, Systems & Control Letters, vol. 162, April 2022, [journal](https://www.sciencedirect.com/science/article/pii/S0167691122000421), [arxiv](https://arxiv.org/abs/2108.07634)
* Chaffey, Forni, Sepulchre, *Scaled Relative Graphs for system analysis*, 2021 IEEE CDC, winner of the Oustanding Student Paper Award [arxiv](https://arxiv.org/abs/2103.13971)
* Chaffey, Padoan, *Circuit Model Reduction with Scaled Relative Graphs*, 2022 IEEE CDC [arxiv](https://arxiv.org/abs/2204:01434)

### Collaborators
* [Rodolphe Sepulchre](https://sites.google.com/site/rsepulchre/), University of Cambridge
* [Fulvio Forni](https://sites.google.com/site/fulvioforni/), University of Cambridge
* [Alberto Padoan](https://albertopadoan.com), ETH Zurich

## Monotone circuits

@@im-50
![circuit](/assets/images/monotone-circuit.svg)
@@

This project explores the connections between nonlinear electrical circuits, modern methods in large-scale optimization, and the input/output approach to nonlinear system theory, pioneered by George Zames.  

The mathematical property of *monotonicity* was born in the study of nonlinear circuits in the early 1960s, in the work of George Minty (known also for the [Klee-Minty cube](https://en.wikipedia.org/wiki/Klee%E2%80%93Minty_cube)).  Monotonicity means energy-dissipating, loosly speaking, and it is closely related to the property of incremental passivity, studied by Zames around the same time.  Monotonicity has since become a fundamental property in the theory of large-scale optimization.  

Revisiting the study of nonlinear circuits using modern monotone optimization techniques has lead to a new algorithmic method for solving nonlinear circuits.  The method uses a *splitting algorithm*, where the splitting corresponds to the circuit interconnection structure.  Searching for splitting algorithms that match circuit structures has also lead to a new splitting method, the *nested forward/backward splitting*, which matches arbitrary series/parallel interconnections.  This method can be used to solve the circuit shown above - an example with $n=100,000$ is shown below.  An alternate method is to use element extraction to express the circuit as the sum of a monotone operator, containing the elements, and a skew-symmetric operator, representing the circuit interconnection.  The Condat--V\~u algorithm can then be applied to solve the circuit behavior.

The property of monotoncity can be used to understand systems with self-sustaining oscillations, modelled as the difference of two monotone systems.  Such systems include the FitzHugh-Nagumo model of an excitable neuron, and the Amari model of lateral inhibition.

@@im-50
![circuit output](/assets/images/monotone-output.svg)
@@

### Publications
* Chaffey, Sepulchre, *Monotone one-port circuits*, IEEE Transactions on Automatic Control, 2023 (early access), [journal](https://ieeexplore.ieee.org/document/10121908), [arxiv](https://arxiv.org/abs/2111.15407), [code](https://github.com/ThomasChaffey/monotone-one-port-circuits)
* Chaffey, Banert, Giselsson, Pates, *Circuit Analysis using Monotone+Skew Splitting*, European Journal of Control, Special Issue for the 2023 European Control Conference, [journal](https://doi.org/10.1016/j.ejcon.2023.100854), [arxiv](https://arxiv.org/abs/2211.14010), [code](https://github.com/ThomasChaffey/circuit-analysis-using-monotone-skew-splitting)
* Chaffey, Sepulchre, *Monotone RLC Circuits*, 2021 European Control Conference, winner of the Best Student Paper Award, [arxiv](https://arxiv.org/abs/2012.11533)
* Das, Chaffey, Sepulchre, *Oscillations in Mixed-Feedback Systems*, Systems & Control Letters, vol. 166, August 2022, [journal](https://www.sciencedirect.com/science/article/pii/S0167691122000998), [arxiv](https://arxiv.org/abs/2103.16379)
* Chaffey, Padoan, *Circuit Model Reduction with Scaled Relative Graphs*, 2022 IEEE CDC [arxiv](https://arxiv.org/abs/2204:01434)

### Collaborators
* [Rodolphe Sepulchre](https://sites.google.com/site/rsepulchre/), University of Cambridge
* [Amritam Das](http://amritamdas.com/), KTH Royal Institute of Technology
* [Fulvio Forni](https://sites.google.com/site/fulvioforni/), University of Cambridge
* [Alberto Padoan](https://albertopadoan.com), ETH Zurich
* [Pontus Giselsson](https://www.control.lth.se/personnel-old/pontus-giselsson/), Lund University
* [Sebastian Banert](https://www.lunduniversity.lu.se/lucat/user/a76b6f949674be884b44ee412a8740e2), Lund University
* [Richard Pates](https://www.richardpates.com/), Lund University

## Differential control synthesis

Differential analysis methods, popularized in systems and control by Winfried Lohmiller and Jean-Jaques Slotine in 1998, involve the analysis of a nonlinear dynamical system via the analysis of its linearization along trajectories, or its *differential dynamics*.  The differential dynamics describe the behaviour of the system in a small neighbourhood of a trajectory.  The approach is made tractable by enforcing some sort of uniformity over the differential dynamics.  Contraction analysis is the differential analysis of stability - loosely speaking, if the differential dynamics are stable in every locality with some minimum rate of convergence, then the global system is also stable. 

Recent work by Ian Manchester and Jean-Jacques Slotine studies the corresponding stabilizability problem: if the differential dynamics are stabilizable in every locality, with some minimum rate of convergence, then the global system is stabilizable.  A global controller can be constructed from a family of differential controllers.  

My work expands the class of controllers that can be used, to include those that don't come from quadratic Lyapunov functions.  This allows some interesting controllers to be constructed, such as controllers which push harder going from $a$ to $b$ than they do from $b$ to $a$.  This is sensible:  I'd like my controller to work hard pushing a bicycle up a hill, but not to work very hard at all rolling it back down!

### Publications
* Chaffey, Manchester, *Control Contraction Metrics on Finsler Manifolds*, 2018 American Control Conference, [arxiv](https://arxiv.org/abs/1803.01034)

### Collaborators
* [Ian Manchester](http://www-personal.acfr.usyd.edu.au/ian/bio/), University of Sydney

# Contact
tlc37 [at] cam.ac.uk

Thomas Chaffey,
Department of Engineering,
University of Cambridge,
Trumpington Street,
CB2 1PZ Cambridge, UK
