+++
title = "Thomas Chaffey"
hascode = true
date = Date(2023, 08, 22)
rss = "Research in nonlinear control systems, circuits and optimization."
+++
@def tags = ["control", "research", "circuits", "optimization"]

Lecturer, [School of Electrical and Computer Engineering, University of Sydney](https://www.sydney.edu.au/engineering/about/our-people/academic-staff/thomas-chaffey.html)

# Open positions
I have open PhD positions in my group at the University of Sydney. For more information, see [this page](https://www.sydney.edu.au/research/opportunities/3625.html).

# Updates

* *09/05/2025* My paper with Fulvio Forni on a novel describing function method utlising square waves rather than sinusoids has been accepted for presentation at the European Control Conference in June.  The paper is titled [Amplitude response and square wave describing functions](https://arxiv.org/abs/2412.01579)
* *09/05/2025* The following tow papers have been submitted to the 2025 IEEE Conference on Decision and Control: [On phase in scaled graphs](https://arxiv.org/abs/2504.21448), [Graphical Dominance Analysis for Linear Systems: A Frequency-Domain Approach](https://arxiv.org/abs/2504.14394).
* *02/04/2025* Together with Arjan van der Schaft and Rodolphe Sepulchre, we have posted a preprint titled [Symmetry in linear physical systems](https://arxiv.org/abs/2504.02062), which explores geometric characterisations of various symmetric structres that arise in models of physical systems.
* *15/03/2025* We just posted a [preprint](https://arxiv.org/abs/2503.00349) on convergence of energy based learning algorithms in circuits which learn.

# Research interests
My research lies at the intersection of nonlinear control theory, convex optimisation, circuit theory and neural networks.  Particular interests include:

* analogue neuromorphic circuits
* graphical analysis and design methods
* monotone operator methods in large-scale optimization
* the interplay between circuit theory and convex optimisation.

I love searching for connections between the latest research topics and old, forgotten ideas.  My two biggest heros are probably [Jan Willems](https://homes.esat.kuleuven.be/~sistawww/smc/jwillems/) and [George Zames](http://www.mit.edu/~mitter/publications/85_legacy_zames_IEEEAC.pdf).

# Publications
For a full list of publications, see my [Google Scholar page](https://scholar.google.nl/citations?user=mpR3WKgAAAAJ&hl=en).  A copy of my PhD thesis can be downloaded [here](/assets/pdf/Tom_thesis.pdf).  Please let me know if you find any typos.

# Bio

From 2022 to 2025, I held the Maudslay-Butler Research Fellowship at Pembroke College, University of Cambridge.  I completed my PhD in April 2022 in the Control Group, University of Cambridge, supervised by [Rodolphe Sepulchre](https://sites.google.com/site/rsepulchre/).  From August 2022, I spent seven weeks as a visiting researcher in the Department of Automatic Control at Lund University, Sweden.  My undergraduate degree was in mathematics and computer science, and my masters was in mechanical engineering, both at the University of Sydney, Australia.  I'm a qualified welder, and I love rock climbing, cycling, surfing and music (especially Bach and anything with a time signature of 7).

In 2023 I was interviewed for the [IEEE Control Systems "PhDs in Control" column](https://ieeexplore.ieee.org/document/10015605).


# Projects

## Learning in physical systems

This project studies approaches to learning directly in analogue electronic hardware.  A convex optimization view is taken to distributed learning algorithms such as contrastive learning, which may be implemented in hardware.  The aim is to inform the design of both hardware and algorithms, by developing a rigorous theory of convergence, and drawing on classical circuit theory to characterise the expressive power of various designs.

### Main publications
* Huijzer, Chaffey, Besselink, van Waarde, *Convergence of energy-based learning in linear resistive networks*, under review, [arxiv](https://arxiv.org/abs/2503.00349)

### Collaborators
* [Henk van Waarde](https://henkvanwaarde.github.io/), University of Groningen
* [Bart Besselink](https://www.math.rug.nl/~besselink/), University of Groningen


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

### Main publications
* Chaffey, Sepulchre, *Monotone one-port circuits*, IEEE Transactions on Automatic Control, 2024, [journal](https://ieeexplore.ieee.org/document/10121908), [arxiv](https://arxiv.org/abs/2111.15407), [code](https://github.com/ThomasChaffey/monotone-one-port-circuits)
* Chaffey, Banert, Giselsson, Pates, *Circuit Analysis using Monotone+Skew Splitting*, European Journal of Control, Special Issue for the 2023 European Control Conference, [journal](https://doi.org/10.1016/j.ejcon.2023.100854), [arxiv](https://arxiv.org/abs/2211.14010), [code](https://github.com/ThomasChaffey/circuit-analysis-using-monotone-skew-splitting)
* Chaffey, van Waarde, Sepulchre, *Relaxation Systems and Cyclic Monotonicity*, 2023 IEEE Conference on Decision and Control, [arxiv](https://arxiv.org/abs/2312.03389)
* Shahhosseini, Chaffey, Sepulchre, *An operator-theoretic framework to simulate neuromorphic circuits*, 2024 IEEE Conference on Decision and Control, [proccedings](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10886469)

### Collaborators
* [Rodolphe Sepulchre](https://sites.google.com/site/rsepulchre/), University of Cambridge
* [Amritam Das](http://amritamdas.com/), KTH Royal Institute of Technology
* [Fulvio Forni](https://sites.google.com/site/fulvioforni/), University of Cambridge
* [Alberto Padoan](https://albertopadoan.com), University of British Columbia
* [Pontus Giselsson](https://www.control.lth.se/personnel-old/pontus-giselsson/), Lund University
* [Sebastian Banert](https://www.lunduniversity.lu.se/lucat/user/a76b6f949674be884b44ee412a8740e2), Lund University
* [Richard Pates](https://www.richardpates.com/), Lund University
* [Henk van Waarde](https://henkvanwaarde.github.io/), University of Groningen
* [Amir Shahhosseini](https://scholar.google.com/citations?user=1AUGWr4AAAAJ&hl=en), KU Leuven

## Scaled Relative Graphs and nonlinear system analysis

@@im-50
![SRG](/assets/images/srg.svg)
@@
Scaled Relative Graphs (SRGs) are a new tool in optimization, developed by [Ernest Ryu, Robert Hannah and Wotao Yin](https://link.springer.com/article/10.1007/s10107-021-01639-w) for the study of convergence of optimization algorithms.  My project studies the relationship between the SRG and the classical Nyquist diagram of LTI control theory.  

The SRG is a generalization of the Nyquist diagram to stable nonlinear operators.  Like the Nyquist diagram, the SRG can be used to determine when a feedback system will be stable.  Studying stability with SRGs gives a graphical unification of many existing results on incremental stability, and opens up an entirely new avenue for studying nonlinear system properties.  Particularly interesting properties include nonlinear robustness margins defined as distances between SRGs.  

The figure above shows an analytical SRG of an LTI transfer function (left, Nyquist diagram in black), and a sampling of the SRG of Hodgkin and Huxley's potassium conductance (right).

Some code for plotting SRGs is available [here](https://github.com/ThomasChaffey/Linear-SRG).

### Main publications
* Chaffey, Forni, Sepulchre, *Graphical Nonlinear System Analysis*, IEEE Transactions on Automatic Control, 2023 (early access), [journal](https://ieeexplore.ieee.org/document/10005799), [arxiv](https://arxiv.org/abs/2107.11272)
* Chaffey, *A rolled-off passivity theorem*, Systems & Control Letters, vol. 162, April 2022, [journal](https://www.sciencedirect.com/science/article/pii/S0167691122000421), [arxiv](https://arxiv.org/abs/2108.07634)
* van den Eijnden, Chaffey, Oomen, Heemels, *Scaled graphs for reset control system analysis*, European Journal of Control, 2024 (early access), [journal](https://www.sciencedirect.com/science/article/pii/S0947358024001109?via%3Dihub)

### Collaborators
* [Rodolphe Sepulchre](https://sites.google.com/site/rsepulchre/), University of Cambridge
* [Fulvio Forni](https://sites.google.com/site/fulvioforni/), University of Cambridge
* [Alberto Padoan](https://albertopadoan.com), University of British Columbia
* [Sebastiaan van den Eijnden](https://research.tue.nl/en/persons/sebastiaan-jam-van-den-eijnden), TU Eindhoven
* [Chao Chen](https://research.manchester.ac.uk/en/persons/chao-chen), University of Manchester
* [Andrey Kharitenko](https://nccr-automation.ch/index.php/about/people/andrey-kharitenko), ETH Zurich


# Contact
thomas.chaffey [at] sydney.edu.au

Thomas Chaffey,
School of Electrical and Computer Engineering
University of Sydney,
NSW 2006, Australia
