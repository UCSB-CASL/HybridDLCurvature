# Level-Set Curvature Neural Networks: A Hybrid Approach

This is the accompanying repository for our *hybrid inference system* that approximates mean curvature in the level-set method.
The neural networks here available were trained on the negative curvature spectrum, with samples from two-dimensional circular 
and sinusoidal interfaces.  We considered 4 different mesh sizes: 2^{-7}, 2^{-8}, 2^{-9}, and 2^{-10}.  We have grouped the 
corresponding models into 4 folders: `7`, `8`, `9`, and `10`.  These numbers also represent the maximum levels of refinement of 
the quadtrees we used in our C++ parallel level-set library.

You'll find in each folder:
- The trained model (in `*.h5` format), 
- The pickled transformer object (`PCA`) for data preprocessing,
- Some stats, and 
- Two plots comparing the numerical (`scatterNumerics.png`) and the neural (`scatterReinit.png`) approximations 
to mean curvature for (train + test + validation) samples obtained with level-set (10-iteration, PDE) reinitialization.

Feel free to forward your questions to [lal@cs.ucsb.edu](mailto:lal@cs.ucsb.edu).
