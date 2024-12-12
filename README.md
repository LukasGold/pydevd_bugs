[![Project generated with PyScaffold](https://img.shields.io/badge/-PyScaffold-005CA0?logo=pyscaffold)](https://pyscaffold.org/)

# pydevd_bugs

> Minimal example for pydevd plugin bugs in PyCharm

# Bugs

## co_lnotab deprecated

Debugging ./examples/trigger_types_warning.py should trigger the following warning:
```
C:\Program Files\JetBrains\PyCharm Professional\plugins\python-ce\helpers\pydev\_pydevd_bundle\pydevd_collect_try_except_info.py:157: DeprecationWarning: co_lnotab is deprecated, use co_lines instead.
  if not hasattr(co, co_line_attr_name):
```
To reproduce, consider reusing a virtual environment created with from a miniforge installation with python 3.12.7 
and the packages specified within requirements.txt. Simply create the environment and install this project in 
editable mode with 
```
pip install -e . 
```