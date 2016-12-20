# Upload package to PyPi

##### Whats is Pypi?
 
  
> The Python Package Index is a repository of software for the Python programming language.

##### GitHub


##### Create your account
For the first step is necessary that you have an active count in [pypi]

---

###### Files
You need create a couples of new files (These file are not in your package) 
    
  - LICENCE.txt
  - README.md
  - setup.cfg
  - setup.py
  - .pypirc
  
   
###### LICENCE.txt
If you don´t have any idea about what kind of licence use, I advise you use [MIT] licence.
Just need copy, paste and replace some words 

###### README md
Like other readme md file

###### setup.cfg

```Python
[metadata]
description-file = README.md
```
###### setup.py

```Python

from distutils.core import setup

setup(
  name = 'package_name',
  packages = ['package_name'],
  version = '0.0.1',
  description = 'Some little description, this description will be showed in the web page',
  author = 'Eduardo Ismael García Pérez',
  author_email = 'email@contact',
  url = 'github url',
  keywords = ['', '', ''],
  classifiers = [],
)
    
```
###### .pypirc

```python
[pypi]
repository=https://pypi.python.org/pypi
username=your_username
password=your_password
```
That`s all, you will finish with this stuct:

![alt tag](http://imgur.com/U9JlyG2.png=10x20)

> Note: .pypircs is not visible
---

##### Upload Package

```python
python setup.py register -r pypi
```

then 

```python
python setup.py sdist upload -r pypi
```

Congratulations, now you are Contributed to python community.

[pypi]: <https://github.com/doorkeeper-gem/doorkeeper>
[MIT]: <http://opensource.org/licenses/MIT>



