# python_intro_notes
python_intro_notes

### Running python 3 on Windows
On mac and linux after installing python 3 you can just run `python3` or `python3.7` to run a specific version if you have multiple python3 versions.

Sadly on windows things are a bit more complicated. There is no `python3` command, you can run `python` to run python3 if python 2 ins't installed but if it is you'll have to run  `py -3 c:/path/to/script` or `py -37 c:/path/to/script` or supply the fullpath `c:\Python37\python -m  pip install lxml`

Any command using `python3` will have to be adjusted to use the py launcher or full path to python
### Running python modules

In python some modules can be used similarly to scripts without specifying the path to them.
This can be useful (especially for running pip and IPython)

example

`curl http://api.joind.in | python -mjson.tool`

to format json

`python3 -m http.server` to start an insecure http test/quick file share server (ctrl-C to exit)



# to install extra libraries

run 

`pip install pandas lxml`

and if for some reason pip isn't installed on PATH or you have multiple python install's and want to pick a particular pip/python sitelib

you can run

`python -m pip install pandas lxml`

# virtualenv

virtualenv is a way to install python libraries (for a particular installation of python)  
to a particular directory instead of installing it globally or per user.
You activate the virtualenv and then running python will pick up that python installation and those and only those libraries in that directory.

The use of  virtualenv and virtualenvwrapper (a wrapper for virtualenv dirs) is beyond this short tutorial.

see https://docs.python-guide.org/dev/virtualenvs/ for more info.

pycharm also has a really nice gui for controlling/using virtualenvs (search for Interpeter in pycharm settings)

# IPython
Python is an interactive dynamic language.  
One of the best ways to understand it is to run code in a python shell and see what happens.  
Sadly the default shell you get when you type `python3` (without providing a script or module) isn't very good(to see what I mean try exiting with ctrl-c).  
Nearly the first thing I recommend for every person learning python is to install IPython.

IPython shell is an amazing exploratory shell. 

Run `python3 -m pip install ipython[notebook]` to install ipython and its notebook mode

Run `python3 -m IPython` to run IPython

# IPython Notebook

IPython was developed by scientists for scientific programming.

They were used to Maple and Mathematica which mixed some code with math equations and graphs and explanations all in one sheet.

They developed IPython Notebook mode to allow interactive based presentations that can be used for science or tutorials like this one.

ipython notebook allows you to mix rendered markdown, rendered HTML, runnable code blocks(in python or a mix of many other languages), Images (mostly of graphs/charts but can be anything like say a screenshot of a remotely controlled desktop), widgets with javascript.

https://github.com/jupyter/jupyter/wiki/A-gallery-of-interesting-Jupyter-Notebooks

An intresting example:

https://nbviewer.jupyter.org/github/rjtavares/football-crunching/blob/master/notebooks/an%20exploratory%20data%20analysis%20of%20the%20world%20cup%20final.ipynb

It's also more useful the ipython (shell) for certain kinds of interactive/explorative programming(usually involving data manipulation). 

I've found it incredibly helpful when trying to understand an undocumented loosely structured noqsl database I inherited ownership off.



# Running these workbooks

You can run these workbooks by installing ipython notebook and downloadin them or running it online in binder

https://mybinder.org/v2/gh/rtaycher/python_intro_notes/master

