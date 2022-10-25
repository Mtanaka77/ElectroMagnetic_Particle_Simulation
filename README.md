## Low-Frequency Electromagnetic Particle Simulation for High-Temperature Plasmas ##

Why is a current sheet of the distant magnetotail of the earth to be thinned and why is a large energy to be released, which is typically observed as magnetic reconnection ? There were many theories for the reconnection including from classical Dungey's theory to nuclear-fusion oriented anomalous resistivity. It is noted that Dr. Speicer in the mean time paid attention to inertia resistivity of thinning the neutral sheet. Some time later in 1995 (Ref.3), a particle simulation was executed to have shown the reconnection mechanism as different inertia of ions and electrons to result in large energy release of earth's magnetotail.

An electromagnetic particle simulation code is thus utilized for solar and magnetospheric space physics. Both electric and magnetic fields at low frequencies are solved by a slightly backward time decentering technique. Magnetic reconnection and the solar wind-earth magnetic field coupling are quite suitable for applying this simulation code.

One uses here the time decentered scheme in aimpl=0.6, while the time centered scheme in the explicit code (aimpl=0.5) is used in other directory of molecular dynamics simulations. It is noted, however, that finite errors in the divergence term accumulate which must be corrected if the finite difference coordinate space are utilized. Four physical units are, i) time: 1/wpe (c/wpe: electron inertia length), ii) length: c/wpe, iii) mass: electron mass, and iv) charge: electron charge. The program is written in Fortran 2003 and is coded for parallelization at MPI version 3.

By the implicit scheme it is free from the Courant condition, that is, Dx(length)/Dt(time step) >< c, the speed of light. For the backward differential scheme in aimpl > 0.5, a time step may be used as dt~1.2/wpe to dump out plasma oscillations, while 2 \pi/dt wce > 1 for the kinetic ions and electrons. A large time step of 2 \pi/dt wce >> 1 is a good target of the drift-kinetic simulation, where a typical time step may be dt= 10/wpe.

One can enjoy simulations by changing system sizes and boundary conditions. For the present case, an equilibration of the pair of flux bundles is first tested in three dimensions. Fully kinetic ions and electrons are simulated in the igc=1 case specified, for example, in the rec_3d13A file. Then, start looking at a merging of flux bundles. 
On the other case, the drift-kenetic electrons and kinetic ions are simulated as a large time step in the igc=2 case. But, one should note that heavy ions move kinetically while light electrons lose some of their particle freedom in the coordinate space.

Easy in-house graphic plots are incorporated in "@mrg37-013A.f03" in order to check the current run in the simulation. 
Figure 1 in the PDF plot "EMfield.pdf" shows the electric and magnetic fields in YZ and X at the early and final times. 
Reading papers of this implicit particle simulation code (Ref. 1-2) and applications to magnetospheric space plasmas (Ref. 3-5) are highly recommended.


References:

1. M. Tanaka, A simulation of low-frequency electromagnetic phenomena in kinetic plasmas of three dimensions, J.Comput. Phys., 107, 124-145 (1993).

2. M. Tanaka, Macro-EM particle simulation method and a study of collisionless magnetic reconnection, Comput.Phys.Commun., 87, 117-138 (1995).

3. M. Tanaka, Macro-particle simulations of collisionless magnetic reconnection, Phys.Plasmas, 2, 2920-2930 (1995).

4. M. Tanaka, Asymmetry and thermal effects due to parallel motion of electrons in collisionless magnetic reconnection, Phys.Plasmas, 3, 4010-4017 (1996).

5.  H. Shimazu, M. Tanaka, and S. Machida, The behavior of heavy ions in collisionless parallel shocks generated by the solar wind and planetary plasma interactions, J.Geophys.Res., 101, 27565-27571 (1996).


