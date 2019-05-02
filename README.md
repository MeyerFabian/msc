Presentation can be found at: https://github.com/MeyerFabian/msc/blob/master/pres/pres.pdf.

Abstract
====
The material point method is allowing for physically based simulations. It has found its way into computer graphics and since then rapidly expanded. The material point method’s hybrid use of Lagrangian particles as a persistent storage and a background uniform Eulerian grid enables solving of various partial differential equations with ease.

The material point method suffers from high execution times and is thus only viable for hero shots. The method is however highly parallelizable. Thus, this thesis proposes how to accelerate the material point method using GPGPU techniques. Core of the material point method are grid and particles transfers that interpolate between the two structures. These transfers are executed multiple times per physical time step. Preprocessing steps might be taken if their computing time is outweighed.

Deep sorting with counting sort increases coalescing and L2 cache hit rates. Binning allows to divide the grid into blocks for shared memory filtering techniques. All operations do not rely on fixed bin size. As another preprocessing step, only grid blocks are executed which have particles in them.

