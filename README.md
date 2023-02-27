# Demo Python Library

Create a python lib on git.

## Create Library

- Create setup.py

```python
from setuptools import setup

setup(
    name='demo_python_lib',
    version='0.0.11',
    description='Demo python lib from git',
    url='https://github.com/500ping/demo_python_lib',
    author='Thang Nguyen',
    author_email='ndt512x@gmail.com',
    packages=['demo_python_lib'],
    # install_requires=[
    #     'requests>=2.25.1',
    #     'tqdm>=4.59.0'
    # ]
)
```
- Create tag 
```bash
git tag 0.0.11
git push --tags
```
- File structure
```bash
demo_python_lib/
├── demo_python_lib/
│   ├── __init__.py
│   └── test1.py
├── setup.py
└── README.md
```

## Install lib
- Add requirements.txt

```bash
demo-python-lib @ git+ssh://git@github.com/500ping/demo_python_lib.git@0.0.11
```
- pyproject.toml (Poetry)
```bash
demo_python_lib = {git = "ssh://git@github.com/500ping/demo_python_lib.git", rev = "0.0.11"}
```
- install 
Pip
```bash
pip install setuptools wheel
pip install -r requirements.txt
```
Poetry
```bash
poetry install
```
