<p align="center">
  <img alt="Datahugger - Where DOI hugs Data" src="https://github.com/J535D165/datahugger/raw/main/datahugger_repocard_tagline.svg">
</p>

# Datahugger - Where DOI :open_hands: Data

Datahugger is a tool to download scientific datasets, software, and code from a large number of repositories based on their DOI [(wiki)](https://en.wikipedia.org/wiki/Digital_object_identifier) or URL. With Datahugger, you can automate the downloading of data and improve the reproducibility of your research. Datahugger provides a straightforward [Python interface](#download-with-python) as well as an intuitive [Command Line Interface](#download-with-command-line) (CLI).

## Supported repositories

Datahugger offers support for more than [<!-- count -->350<!-- count --> generic and specific (scientific) repositories](https://j535d165.github.io/datahugger/repositories) (and more to come!).

[![Datahugger support Zenodo, Dataverse, DataOne, GitHub, FigShare, HuggingFace, Mendeley Data, Dryad, OSF, and many more](https://github.com/J535D165/datahugger/raw/main/docs/images/logos.png)](https://j535d165.github.io/datahugger/repositories)

We are still expanding Datahugger with support for more repositories. You can
help by [requesting support for a repository](https://github.com/J535D165/datahugger/issues/new/choose) in the issue
tracker. Pull Requests are very welcome as well.

## Installation

![PyPI](https://img.shields.io/pypi/v/datahugger)

Datahugger requires Python 3.6 or later.

```
pip install datahugger
```

## Getting started

### Datahugger with Python

Load a dataset (or any digital asset) from a repository with the
`datahugger.get()` function. The first argument is the DOI or URL
and the second argument the name of the folder to store the dataset (will be
created if it does not exist).

The following code loads dataset [10.5061/dryad.mj8m0](https://doi.org/10.5061/dryad.mj8m0) into
the folder `data`. 

```python
import datahugger

# download the dataset to the folder "data"
datahugger.get("10.5061/dryad.mj8m0", "data")
```

For an example how this can integrate with your work, see the 
[example workflow notebook](https://github/J535D165/datahugger/blob/main/examples/example_datahugger_in_workflow.ipynb) or 
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/J535D165/datahugger/blob/main/examples/example_datahugger_in_workflow.ipynb)


### Datahugger with command line

The command line function `datahugger` provides an easy interface to download data. The first
argument is the DOI or URL and the second argument the name of the folder to store the dataset (will be
created if it does not exist).

```bash
datahugger 10.5061/dryad.31zcrjdm5 data
```

```bash
% datahugger 10.5061/dryad.x3ffbg7m8 data
README_Pfaller_Robinson_20[...].txt: 100%|█████████████████████████████████████| 17.1k/17.1k [00:00<00:00, 2.62MB/s]
Pfaller_Robinson_2022_Glob[...].csv: 100%|████████████████████████████████████████| 709k/709k [00:00<00:00, 904kB/s]
Repository content successfully downloaded.
```

**Tip:** On some systems, you have to quote the DOI or URL. For example: `datahugger "10.5061/dryad.31zcrjdm5" data`. 

## Tips and tricks

- No need to struggle with DOIs versus DOI URLs. They both work (and more). Example: The values `10.5061/dryad.x3ffbg7m8`, `doi:10.5061/dryad.x3ffbg7m8`, [`https://doi.org/10.5061/dryad.x3ffbg7m8`](https://doi.org/10.5061/dryad.x3ffbg7m8), and [`https://datadryad.org/stash/dataset/doi:10.5061/dryad.x3ffbg7m8`](https://datadryad.org/stash/dataset/doi:10.5061/dryad.x3ffbg7m8) all point to the same dataset.
- Do not republish the dataset when you are uploading your data to an scientific data repository. These storages resources can be used better :)

## License

[MIT](/LICENSE)

## Contact

Feel free to reach out with questions, remarks, and suggestions. The
[issue tracker](/issues) is a good starting point. You can also email me at
[jonathandebruinos@gmail.com](mailto:jonathandebruinos@gmail.com).
