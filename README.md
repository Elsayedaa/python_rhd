# RHD

A module for reading Intan RHD2000 files (*.rhd).

Code written by  Michael Gibson 17 July 2015.

Python module first packaged by Kyler Brown 2016.

Modified by Adrian Foy January 2023.

Python module updated and repacked by Ahmad Elsayed May 2023.


## installation
    pip install https://github.com/Elsayedaa/python_rhd/archive/refs/heads/main.zip

    or

    git clone https://github.com/kylerbrown/rhd.git
    cd rhd
    python setup.py install

## usage

    import rhd
    # To keep memory usage down, use argument no_floats=True.
    # Otherwise, data is loaded as floating point arrays
    # (4x the space required).
    data = rhd.read_data("file.rhd", no_floats=True)
    import matplotlib.pyplot as plt
    plt.plot(data['amplifier_data'][:,:1000].T)
    plt.show()
