# Sample Lecture - R

<a href="https://hydrocode.de" target="_blank">
<img src="https://firebasestorage.googleapis.com/v0/b/hydrocode-website.appspot.com/o/public%2Fhydrocode_brand.png?alt=media"  style="height: 60px; float: left" height="60"/></a>

This is a template repository for creating lectures with [Jupyter Notebooks](https://jupyter.org) and publish them
using [Notebook-Classroom](https://github.com/hydrocode-de/notebook-classroom).

The best way to build your own is to [generate a new repository using this as a template](https://github.com/hydrocode-de/sample-lecture-r/generate)

<hr>

## What's contained?

There are a cople of files in the repository. Most of them don't need to be touched, but you can use them to adjust 
this sample lecture to your needs. 

### environment.yml

We putted a pretty complete R environment together, that should get you directly started. We recommond using [anaconda](https://anaconda.com/distribution). You can create a new environment with all neccessary packages included like:

```bash
conda create -f environment.yml -n R
```
Where ``R`` would be the name of the new environment. There is a [cheat sheet](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf) for more info.

You can also update an existing environment like:

```bash
conda env update -f environment.yml -n your_environment
```

Where ``your_environment`` is the name of the **existing** anaconda R environment.

Beside the ``environment.yml``, we also distribute a ``environment.exact.yml``, which fixes **all** packages in the environment to the exact same version as used to create this lecture. Use with causion as some packages might be outdated or not available at that version for your operating system.

### img folder

The ``img`` can be used to add images to your lecture notes, scripts and slides. Just add them as:

```markdown
![name](./img/file_name)
```

This will work in your ``.md`` and ``.ipynb`` files.

### data folder

The ``data`` folder can be used to add data to the repository, which will be used by your scripts 
or is distributed to your students, in case they clone this repository, too.

### static folder

The static folder can be used to add static content to webpage in ``.md`` and ``.html`` format. The only exception from is rule is the ``index.md``, which is also allowed in 
the root directory.

### .ipynb files

The files ending on ``.ipynb`` are the jupyter notebooks. They can be run by ``jupyter lab`` or ``jupyter notebook`` 
and are editable in the browser. Each notebook consists of sequential *cells* that are placed underneath each other to 
compose a document. They can contain images, text, latex code, formulas or code.
There are a number of *kernels* available, these are interpreters (or compiler) to run code added to a code cell. 
In this sample lecture, we will use Python, but C++, R, Julia or Ocatve are also possible.

These files can be distributed as ``.ipynb`` files containing executable code. Then the reciever will need to install jupyter as well.
Alternatively, you can compile the notebook to HTML, PDF of HTML-slides. With this sample project, all notebooks will 
automatically be compiles to HTML and slides and be published on [GitHub Pages](https://pages.github.com/).

## index.md

This file will be used as the landing page of the published [Notebook-Classroom](https://github.com/hydrocode-de/notebook-classroom) application.
Introduce the module here, or give some advice to your students, how these resources 
should be used.

## Great. I want that. So what to do?

1. Add missing packages to the ``environment.yml``
2. Remove/replace all ``.ipynb`` with your lectures
3. Configure [Notebook-Classroom](https://github.com/hydrocode-de/notebook-classroom) application by adjusting [configuration.js](configuration.js).
