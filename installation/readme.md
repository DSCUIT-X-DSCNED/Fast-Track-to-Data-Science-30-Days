
### Index

- [Python Installation](<###\ Python\ Installation>)
- [Path Configuration (Windows only)](<###\ Path\ Configuration\ (Windows\ only)>)
- [What is PIP?](<###\ What\ is\ PIP?>)
- [How does Python code run?](<###\ How\ does\ Python\ code\ run?>)
- [Running Python: **Interactive shell (terminal)**](<###\ Running\ Python:\ **Interactive\ shell\ (terminal)**>)
- [Running Python: **Interactive Python notebooks (Jupyter Notebook/Google Colab)**](<###\ Running Python: **Interactive Python notebooks (Jupyter Notebook/Google Colab)**>)
- [Running Python: **Scripts**](<###\ Running\ Python:\ **Scripts**>)

By _Tarun Kumar_, Python@DSU Lead and Core Team member

With hopes of imparting my knowledge in a befitting manner to you, we start the bootcamp. The main aim of this series will be to become a source I wish I had when I was stuck in the dive in barrier people usually have when starting something new. So let's get started without any further ado?

Python holds quite some importance as a language in software development, considering it keeps rocking the "Most Wanted" language developers want to work with in **_Stackoverflow Developer Survey_** of [2020](https://insights.stackoverflow.com/survey/2020#most-loved-dreaded-and-wanted), [2019](https://insights.stackoverflow.com/survey/2019#most-loved-dreaded-and-wanted), [2018](https://insights.stackoverflow.com/survey/2018#most-loved-dreaded-and-wanted)

And seeing as you came upon here, you're probably one of them.

[Installing Python](<###\ Python\ Installation\ and\ Setup>)

### Python Installation

Now you might hear people suggesting that you can install Anaconda package as it installs everything that you may require in the near future to learn and work with Python? While that might be true for mathematicians, scientists or less tech-savvy who just want to start running a script without caring much about tinkering a bit to configure stuff, **_hackers_** like us don't do it that way.

Since OSX comes pre-installed with Python and people using Linux distros already know how to apt-get their packages, I would keep this limited to Windows users.

1. To begin installation in a vanilla way, you can download the respective installer from [Download Python | Python.org](https://www.python.org/downloads/)
2. Run the installer

<img src="Lecture%20Notes%2006f7e20d1f064197ad83d6ed5d75fc11/Untitled.png" width="500"/>

Remember the path being mentioned here.

The default install path is in the AppData/ directory of the current Windows user.

Keep "Add Python 3.8 to PATH" unselected

3. Voila, you have Python installed on your Windows machine.

### Path Configuration (Windows only)

However you cannot start programming with Python yet, atleast not on a system-wide level. To do so, you must configure your PATH so that Windows knows what Python is.

To do so:

1. Press windows key

2. Search for "environment variables" and open "Edit the system environment variables"

<img src="Lecture%20Notes%2006f7e20d1f064197ad83d6ed5d75fc11/Untitled%201.png" width="500"/>

3. Click the environment variables button:

<img src="Lecture%20Notes%2006f7e20d1f064197ad83d6ed5d75fc11/Untitled%202.png" width="500"/>

4. In the bottom dialog(system variables), click on the variable with name PATH and click edit

<img src="Lecture%20Notes%2006f7e20d1f064197ad83d6ed5d75fc11/Untitled%203.png" width="500"/>

5. Click on new button and paste in the following

1) Path where we installed Python in step 2, for me it was:

```bash
C:\Users\Tarun\AppData\Local\Programs\Python\Python39
```

<img src="Lecture%20Notes%2006f7e20d1f064197ad83d6ed5d75fc11/Untitled%204.png" width="500"/>

2. Same path as above with the addition of **\Scripts** at the end.

```bash
C:\Users\Tarun\AppData\Local\Programs\Python\Python39\Scripts
```

<img src="Lecture%20Notes%2006f7e20d1f064197ad83d6ed5d75fc11/Untitled%205.png" width="500"/>

6. Voila, you can now run Python in your system. To verify that you've done everything correctly just open a command prompt window or PowerShell window and just type in:

```bash
python --version
```

You shall get a response similar to this,

<img src="Lecture%20Notes%2006f7e20d1f064197ad83d6ed5d75fc11/Untitled%206.png" width="500"/>

if you don't, make sure you've followed the steps correctly, alternatively you can watch the video for today's lecture.

### What is PIP?

In a modern language, libraries and frameworks allow you to use existing codebase to fast-track your development. You don't necessarily need to reinvent the wheel for most cases if the existing solution has had years of development and is probably faster than whatever you could write.

So in such cases, you may use existing code that is written and deployed in modules called **_packages_** that you can conveniently import into your own codebase and start using the **_functions, classes_** and **_objects_** that it provides.

Now to apply a simple interface for the installation and configuration of such packages, Python uses a package manager called **_pip_** which comes pre-installed with a Python installation.

To verify **_pip_** is installed:

```bash
pip --version
```

Output:

<img src="Lecture%20Notes%2006f7e20d1f064197ad83d6ed5d75fc11/Untitled%207.png" width="500"/>

To install any package with pip, you just do:

```bash
pip install package-name
```

To find existing packages that people have created for Python, you can check out **[Py**thon **P**ackage **I**ndex](https://pypi.org/)

### How does Python code run?

In the programming world, **Python** belongs to a family of interpreted (dynamically typed) languages like _JavaScript_, _PHP, Ruby, Perl_ etc.

The advantage of being dynamically typed is that Python does not require the programmer to keep track of variable datatypes and throughout the life of a program, the variable may change not only it's value but also it's datatype. This makes writing code a breeze.

Now the term used to identify programs written in dynamically typed languages (like Python) is "script" and we'll be using the term from here on out.

Now to run Python code, we have three options.

### Running Python: **Interactive shell (terminal)**

Simply open a command prompt or terminal window and type in `python` and you'll enter an interactive shell:

<img src="Lecture%20Notes%2006f7e20d1f064197ad83d6ed5d75fc11/Untitled%208.png" width="500"/>

This can act as a workbench for you to test your code logic before writing it into a script. For example slicing a string, playing with custom formulas etcetera.

## Running Python: **Interactive Python notebooks (Jupyter Notebook/Google Colab)**

**Jupyter Notebooks** are perhaps one of the most comprehensive way to write manuals, documentation, labs, presentations and visualizations using only Python.

To get started with using **Jupyter Notebook**, you need to install the **Jupyter** module using **pip**

Just open CMD/Terminal and write:

```bash
pip install jupyter
```

Now this may take a little while to complete, let it since it's downloading some large dependencies.

Now Jupyter Notebook run on an server environment because it runs a containerized Python kernel which you don't need to confuse yourself with, so just remember to run a local instance of Jupyter Notebook you need to type the following in terminal after installing (using command shown above):

```bash
jupyter notebook
```

This'll launch a [localhost](http://localhost) server and you can view it at [http://localhost:8888/tree](http://localhost:8888/tree) on your browser (running the above command opens it directly)

Now just create a new file:

<img src="Lecture%20Notes%2006f7e20d1f064197ad83d6ed5d75fc11/Untitled%209.png" width="500"/>

You can start writing code in individual cells and execute by pressing `shift + enter`

<img src="Lecture%20Notes%2006f7e20d1f064197ad83d6ed5d75fc11/Untitled%2010.png" width="500"/>

The new file you just created will have the extension `.ipynb` which signifies that the file is an Interactive Python Notebook.

Besides you can use Jupyter Notebooks to write Markdown code as well to provide proper documentation to your presentation. The possibilities are limitless on sharing code that not only you can understand, but you can provide proper documentation so that even a layman may understand what you're trying to do in a code section.

Take a look at this notebook to see the possibilities:

[Exploratory Computing with Python](https://nbviewer.jupyter.org/github/mbakker7/exploratory_computing_with_python/blob/master/notebook1_basics_plotting/py_exploratory_comp_1_sol.ipynb)

If you face the following issue after running `jupyter notebook` on your Windows system:

<img src="Lecture%20Notes%2006f7e20d1f064197ad83d6ed5d75fc11/Untitled%2011.png" width="500"/>

You can fix it by installing the Visual C++ redistributable files from [here](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads)

### Running Python: **Scripts**

Now this is how you'll be spending most of your time on Python. Building scripts that do stuff without any flashy interactive outputs or markdown to explain code.

To write Python scripts, you can:

- use any code editor (Visual Studio Code, Sublime Text, Notepad++ or even Vim if you're badass enough)
- use IDEs (PyCharm, IDLE, Spyder)

I personally love to work on projects that span through multiple languages and frameworks, so Visual Studio Code works for me due to having the lightness of a code editor and great extension support.

You can write code on Word or Google Docs for all Python cares (make sure you convert the code to plaintext first though because it may raise syntax errors otherwise :p ).
