## About svZeroDSolver

svZeroDSolver is a Python code that simulates the hemodynamics in zero-dimensional (0D) lumped parameter models of vascular networks. These 0D models are governed by differential algebraic equations (DAEs).

svZeroDSolver uses a highly modular framework to model the vascular anatomy, using individual 0D elements to represent different parts of the vascular anatomy (and boundary conditions). The individual 0D elements and their associated governing equations defined in `blocks.py`. In `svZeroDSolver.py`, the blocks are assembled and simulated using the generalized-alpha time-stepping method defined in `time_integration.py`.

<!-- add link to the 0D solver and theory documentation on SimVascular website when it is available -->

svZeroDSolver currently supports the following vascular 0D modeling options and boundary conditions:

#### Vascular 0D elements:
- Resistor
- Resistor-capacitor
- Resistor-inductor
- Resistor-capacitor-inductor

#### Boundary conditions:
- Pressure
- Resistor
- RCR
- Coronary
- Flow

### Prerequisites

The following software is required:

- Python 3

The following Python packages are required:

- os
- re
- sys
- pdb
- copy
- numpy
- argparse
- tqdm.tqdm
- importlib
- matplotlib.pyplot
- collections.defaultdict
- scipy
- scipy.interpolate
- scipy.sparse.linalg
- scipy.sparse.csr_matrix

### Execution

~~~
./svZeroDSolver <path to 0D input file>
~~~

Additional options are defined in `svZeroDSolver.py`.
