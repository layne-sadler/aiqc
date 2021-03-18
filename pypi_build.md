# PyPI Package

### Steps to Build & Upload

```bash
pip3 install --upgrade wheel twine

python3 setup.py sdist bdist_wheel

python3 -m twine upload --repository pypi dist/*
# username: __token__
# password: <paste in the token>

# Delete build-generated files before git commit.
rm -r build dist aiqc.egg-info

# Within `setup.py` proactively update the minor version number for next time.
```

### Testing a Fresh Install

```bash
pip freeze | xargs pip uninstall -y
pip install --upgrade aiqc
```