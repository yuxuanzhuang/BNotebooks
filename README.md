# Blender Notebook

A simple command line tool to wrap blender 2.8+ as a jupyter kernel.

Blender's python API requires its embedded python interpreter. As of Blender 2.82, python 3.7 is packaged. In order to make ipykernel and other pip packages accessible to Blender, the `site-packages` directory of the python interpreter executing blender_notebook will be added to Blender's python path. Therefore, it's highly recommended to use exactly the same python version as your blender.

## Installation

The easiest way to install blender_notebook is via pip:
```
$ python -m pip install blender_notebook
```

It can also be installed from source:
```
$ python -m pip install -e .
```

## Usage

If blender in installed by a package manager, the easiest way to find the executable path is:
```
$ which blender
/snap/bin/blender
```
In my case, blender is installed from snap.

Then, run the blender_notebook CLI:
```
$ blender_notebook install --blender-exec /snap/bin/blender
Saving files to ~/.local/share/jupyter/kernels/blender
```

You can also delete the kernel:
```
$ blender_notebook remove
Are you sure to delete ~/.local/share/jupyter/kernels/blender ? [y/N]: y
blender jupyter kernel is removed!
```