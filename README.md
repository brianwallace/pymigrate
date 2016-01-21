# pymigrate

pymigrate is a simple tool used to download packages from a PyPi and for
migrating packages from one repo to another.


## Usage

To use pymigrate, run ```pymigrate download --indexurl INDEX_URL package1 package2 package3```
with the index-url from which packages can be downloaded and the list of packages
to download.

```
$ pymigrate download -i https://pypi.yourcompany.com/simple package1 package2 package3
Downloading |################################| 3/3
Downloaded all externally hosted files, upload to PyPI using `twine upload --skip-existing dist/*`
```

Once that has executed, then run ```twine upload --skip-existing dist/*```
to upload all downloaded files to the PyPi repo of choice.


## To Do

1. Add a upload command (i.e. `pymigrate upload ...` which wraps twine.
1. Add a migrate command (i.e. `pymigrate migrate ...` which wraps twine.
1. Add support for a configuration file which lists packages to migrate.


## Acknowledgements

pymigrate has been based on the [pep470](https://github.com/pypa/pep470) tool.
pymigrate is the start of an attempt to make a more generalized tool python
module migration tool.  pep470 made starting this effort much easier.
