# University of Washington Coursera.org course Machine Learning workspace

## Installation

### Set up Python environment using Anaconda

* Install [Anaconda](https://www.continuum.io/downloads), a package manager and an environment manager for Python.

    conda create -n univ-washington-machine-learning-python-virtualenv python=2.7 anaconda
    source activate univ-washington-machine-learning-python-virtualenv
    conda update pip
    conda update ipython ipython-notebook
    pip install --upgrade --no-cache-dir https://get.dato.com/GraphLab-Create/1.8.4/XXX@gmail.com/6BE1-5664-392B-33BD-D0E7-C4C9-1897-D5C8/GraphLab-Create-License.tar.gz
    
### Alternatively, set up Python environment using virtual environments

* Read the basics of Python virtual environments (`virtualenv`) [^python-virtualenv], [^python-virtualenvwrapper].

* Install Python, `pip`:

        brew install python 

* Make sure `pip` is up-to-date

        pip install --upgrade pip

* Install `virtualenv` packages using `brew`:

        pip install --upgrade virtualenv virtualenvwrapper
    
* Set up virtual environment for this course [^python-vritualenvwrapper-quickstart].

        mkvirtualenv univ-washington-machine-learning-python-virtualenv

  * Customize `bin/postactivate` from [this Git repo](https://github.com/lumeng/univ-washington-machine-learning-python-virtualenv).
  * Activate the new virtual environment

            deactivate # deactivate if already in
            workon
            workon univ-washington-machine-learning-python-virtualenv
            # cd path/to/project

  * Install packages which should be automatically run via `bin/postactivate`, but also alternatively, manually by:
  
            pip install --upgrade pip
            pip install --upgrade "ipython[notebook]"
            pip install --upgrade matplotlib
            pip install --upgrade --no-cache-dir https://get.dato.com/GraphLab-Create/1.8.4/XXX@gmail.com/6BE1-5664-392B-33BD-D0E7-C4C9-1897-D5C8/GraphLab-Create-License.tar.gz            

* Configure matplotlib backend to TkAgg in `~/.matplotlib/matplotlibrc` [^matplotlib-virtualenv-workaround]:

        backend: TkAgg

Alternatively, in Jupyter notebook, run 

        import matplotlib
        #matplotlib.use('qt4agg')
        matplotlib.use('tkagg')

before plotting.
    
## References

[^python-virtualenv]: Python virtual environments (`virtualenv` package), <http://docs.python-guide.org/en/latest/dev/virtualenvs>

[^python-virtualenvwrapper]: Python virtual environment wrappers (`virtualenvwrapper` package), <https://virtualenvwrapper.readthedocs.org>

[^python-vritualenvwrapper-quickstart]: `virtualenvwrapper quick-start, <https://virtualenvwrapper.readthedocs.org/en/latest/install.html#quick-start>

[^matplotlib-virtualenv-workaround]: <http://matplotlib.org/faq/virtualenv_faq.html>

* [Installing and configuring Python on Mac OS X](https://meng6.net/pages/computing/installing_and_configuring/installing_and_configuring_Python_on_Mac_OS_X/)

* [Installing and configuring Python on Ubuntu Linux](https://meng6.net/pages/computing/installing_and_configuring/installing_and_configuring_Python_on_Ubuntu_Linux/)

* Dato.com, [GraphLab package installation guide](https://dato.com/download/install-graphlab-create-command-line.html?email=XXX%40gmail.com&key=6BE1-5664-392B-33BD-D0E7-C4C9-1897-D5C8)
