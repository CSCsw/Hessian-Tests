A collection of simple tests to check the consistency of the hessian computed by:

hessian() in ADOL-C and edge_hess() (which implements the edge_pushing algorithm)

edge_hess() has the same parameters as sparse_hess()
Except a different meaning for options[2]:
    options[0] = 0 (Default)     \\ Disable Preaccumulation
               = 1               \\ Enable Preaccumulation 
                                 \\ (need --enable-preacc when configure ADOL-C)

    options[0] = 0               \\ Use the ADOL-C's location index
               = 1 (Default)     \\ Translate the index into a monotonic sequence

Include the header <adolc/hessian/edge_main.h>
And then call edge_hess() in the same way as if sparse_hess() is called. 
