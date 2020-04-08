# Python Toolkit 

Developing software in Python requires strong knowledge of one's tools. Knowing the quirks of the languages and the best tools will allow one to write better code faster. But to go fast, you need to start slow. Investing time in knowing your tools, shortcut keys, and tricks of the trade will payoff dividends when you have a short deadline or need to fix something on the fly. Below are my recommendations on creating your own Python toolkit that you can take with you wherever you work. 

## IDE

PyCharm. 
* Helpful overview of PyCharm: [PyCharm for Productive Python Development (Guide) – Real Python](https://realpython.com/pycharm-guide/) 
* Configure the Project Interpreter [Configure a Python interpreter - Help \| PyCharm](https://www.jetbrains.com/help/pycharm/configuring-python-interpreter.html)
* Set the correct Testing Framework (default is unittest)
* Merge Conflicts tool
* Compare current state with branch (Git)
* [AWS Toolkit for PyCharm](https://aws.amazon.com/pycharm/)

## Environment

Venv. Whenever you start on a new Python project, don't fuck up your System's Python environment. Leave it alone. Just create a virtual environment. [Creation of virtual environments — Python 3.8.2 documentation](https://docs.python.org/3/library/venv.html)

Pip. Use this as your default package installer. Don't try to memorize all the commands. Just look it up. [Reference Guide — pip 20.0.2 documentation](https://pip.pypa.io/en/stable/reference/) 

Pyenv. If you need to work with different versions of Python, use this tool to switch between versions. [Simple Python version management](https://github.com/pyenv/pyenv)

## Deployment

Travis CI. Use any tool for Continuous Integration. Travis is a good tool and has good documentation. [Building a Python Project - Travis CI](https://docs.travis-ci.com/user/languages/python/)

AWS Boto3. If using AWS to build Python-based software, use Boto3 to do it. [Quickstart — Boto 3 Docs 1.12.37 documentation](https://boto3.amazonaws.com/v1/documentation/api/latest/guide/quickstart.html)

## Source control

[Pre-commit](https://pre-commit.com) uses Git hooks to help automate the formatting and linting of Python code before committing. When used with Black, Flake8, and AutoPEP8 below, it standardizes your code before committing. 

## Formatting and Linting 

[Black](https://github.com/python/black), the uncompromising Python code formatter.

[Flake8](http://flake8.pycqa.org/en/latest/) is a wrapper around various Python linting tools used to check for conformance against the PEP8 style guidelines for Python. This helps make sure that your code is using a consistent style across the entire project.

[AutoPEP8](https://pypi.org/project/autopep8/#pyproject-toml) automatically fixes some PEP8 violations. 

You can configure these tools using pyproject.toml. See [PEP 518 -- Specifying Minimum Build System Requirements for Python Projects \| Python.org](https://www.python.org/dev/peps/pep-0518/)

## Collaboration 

Jupyter. Use this tool to help with collaboration. Install it on your machine; you also get IPython for free. [Overview — Jupyter Documentation 4.1.1 alpha documentation](https://jupyter.readthedocs.io/en/latest/index.html)

## Testing

Pytest. A testing framework that does not require classes to create tests. You simply define a test and run it. It has interesting features like `fixtures` which are an alterantive to a `setup` and `teardown` method ala JUnit. 
[Pytest documentation](http://docs.pytest.org/en/latest/)


Unittest. The default testing framework for Python. Similar to JUnit in that you write tests in an Object-Oriented way. [unittest documentation](https://docs.python.org/3/library/unittest.html#module-unittest)

Coverage. Good tool to measure coverage in a Python program. Good documentation and examples. [Coverage documentation](https://coverage.readthedocs.io/en/coverage-5.0.4/) 

## The Setup Script

Any Python program to be developed and used by others should have and write the setup script. It is the center of all activity in building, distributin, and installing modules. You can use the Disutils library directly, but almost everyone uses the enhanced library Setuptools to write the Setup script. Whenever you develop in Python, writing the Setup script is one of the first things that you should do. 

[Setuptools documentation](https://setuptools.readthedocs.io/en/latest/setuptools.html#installing-setuptools)

[Writing the Setup Script — Python 3.8.2 documentation](https://docs.python.org/3/distutils/setupscript.html)


## Documentation

Sphinx. It's THE tool for Python documentation. [Sphinx documentation](https://www.sphinx-doc.org/en/master/)
And here's a good tutorial: [Sphinx tutorial](https://matplotlib.org/sampledoc/)

reStructuredText is the default markup language used by Sphinx. It's the alternative to Markdown. Yes, it's a pain to learn a new markup language. But reST is not too hard to learn. [reStructuredText  Documentation](https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html)

## Common libraries

Requests. Simply one of the best Python libraries out there in terms of simplicity, design, and user experience. [Requests: HTTP for Humans™ — Requests 2.23.0 documentation](https://requests.readthedocs.io/en/master/)

Json. Make serialization easy for yourself. [JSON encoder and decoder — Python 3.8.2 documentation](https://docs.python.org/3/library/json.html)

Os. You will use this for file opening, writing the setup script, and many other things. [os — Miscellaneous operating system interfaces — Python 3.8.2 documentation](https://docs.python.org/3/library/os.html)

Csv. This. Most common data is in a CSV format. Use this module to make your life easy when processing such files. [csv — CSV File Reading and Writing — Python 3.8.2 documentation](https://docs.python.org/3/library/csv.html)

Urllib. Scrapping the web is a common task. Do it using Python and this module. [urllib — URL handling modules — Python 3.8.2 documentation](https://docs.python.org/3/library/urllib.html)

## Language specific fundamentals

### The Gil

Python is not the best language for writing OOP in my opinion. I prefer Java. But if you must, read this tutorial on Classes in Python. [9. Classes — Python 3.8.2 documentation](https://docs.python.org/3/tutorial/classes.html)

The Global Interpreter Lock aka The GIL. Yes, it's low level information about Python concerning multithreading. But just knowing about it and how it works is a fundamental that every Python programmer should know. [Grok the GIL: How to write fast and thread-safe Python \| Opensource.com](https://opensource.com/article/17/4/grok-gil)

### `if __name__ == "__main__":`

Upon reading a source file, Python will set some special variables (i.e. variables with double underscores) such as __name__ to certain values. This if clause allows the Python program to be run as the main program or if imported into another module, it sets __name__ to the original module. For a deeper dive, read [python - What does if __name__ == "__main__": do? - Stack Overflow](https://stackoverflow.com/questions/419163/what-does-if-name-main-do)

### `__init__.py`

It defines a package as a module. Python executes any code in this file. See [python - What is __init__.py for? - Stack Overflow](https://stackoverflow.com/questions/448271/what-is-init-py-for) for more details. For more on packages and modules, [5. The import system — Python 3.8.2 documentation](https://docs.python.org/3/reference/import.html#regular-packages).
