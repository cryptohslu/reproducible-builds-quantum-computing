# Reproducible Builds for Quantum Computing
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/cryptohslu/reproducible-builds-quantum-computing/HEAD?urlpath=%2Fdoc%2Ftree%2Fnotebooks%2F0_index.ipynb)
[![arXiv](https://img.shields.io/badge/arXiv-2510.02251-b31b1b.svg)](https://arxiv.org/abs/2510.02251)

Supplemental material for the paper ["Reproducible Builds for Quantum Computing"](https://arxiv.org/abs/2510.02251).

## Jupyter notebooks

The [notebooks](./notebooks) directory contains Jupyter notebooks with more technical details of all the examples
described in Sections 6 and 7. You can run these notebooks on the cloud [here](https://mybinder.org/v2/gh/cryptohslu/reproducible-builds-quantum-computing/HEAD?urlpath=%2Fdoc%2Ftree%2Fnotebooks%2F0_index.ipynb)
using [Binder](https://mybinder.org/).

Alternatively, if you prefer to run them locally on your computer, we recommend creating a Python virtual enviroment and
starting Jupyter lab there.

```console
git clone --recurse-submodules https://github.com/cryptohslu/reproducible-builds-quantum-computing.git
cd reproducible-builds-quantum-computing
python -v venv venv
source venv/bin/activate
pip install -r requirements.txt
venv/bin/jupyter-lab
```

> [!TIP]
> Depending on your operating system, you might need to install some additional dependencies to make everything work
> locally. On Debian, use:
> ```console
> sudo apt install graphviz libarchive-dev xxd
> ```

## Qiskit transpilation plugins
The [qiskit_plugins](./qiskit_plugins) directory contains the ready-to-use Qiskit transpilation plugins implementing the
examples from Section 6. These are already installed in your Python virtual environment if you run the previous commands.
If you want to install them on a different virtual environment the easiest way to install them is using `pip` to fetch
the latest versions from [PyPI](https://pypi.org/search/?q=qiskit-leaky).

```console
pip install qiskit-leaky-layout qiskit-leaky-init qiskit-leaky-scheduling
```

Alternatively, you can also install them locally. First, activate the Python virtual environment you want to use and
then run:

```console
cd qiskit_plugins/qiskit-leaky-layout && pip install .
cd ../qiskit-leaky-init && pip install .
cd ../qiskit-leaky-scheduling && pip install .
```

## Acknowledgements

This work was supported by the Swiss National Science Foundation Practice-to-Science Grant No 199084.

## Citation

```bibtex
@misc{arXiv2510.02251,
  title={Reproducible Builds for Quantum Computing},
  author={Iyán Méndez Veiga and Esther Hänggi},
  year={2025},
  eprint={2510.02251},
  archivePrefix={arXiv},
  primaryClass={quant-ph},
  url={https://arxiv.org/abs/2510.02251},
}
```
