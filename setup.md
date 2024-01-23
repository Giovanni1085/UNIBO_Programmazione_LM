# Setting-up your working environment

## Basic option: Binder

[Binder](https://mybinder.org/) allows you to run notebooks in the cloud via your browser. Just click on launch Binder in the repo. Remember to download any file you edited and want to preserve.

## Recommended option: Anaconda or Edupyter

First, download the data and code for each class. Go to [the course's repository](https://github.com/Giovanni1085/UNIBO_Programmazione_LM) and click on download > zip (top right). Unzip locally somewhere you know (e.g., Documents folder). Keep in mind that you will need to download again when new contents are added to the repository.

[Jupyter Notebooks](https://jupyter.org/) allow you to code and type in your browser. This is included in the Anaconda and Edupyter distribution. Jupyter Lab is a more complete and modular Web environment, you will not need it for this course. Both Anaconda and Edupyter allow you to manage your Python environment and to work with notebooks locally, on your pc.

### Anaconda

1. Install the [Anaconda distribution](https://www.anaconda.com/distribution/), remember to pick any Python from 3.8 to 3.11 and the OS you need. Get the graphical installer. You do not need to install the optional programs, such as the PyCharm editor. 
2. After installation, you will have an app called **Anaconda Navigator** installed. You can create and manage enviromnents and use jupyter notebooks from it, without using the terminal.
3. If you now launch the Jupyter Notebook, it will open a browser window. Navigate to the place where you downloaded and extracted the zip with the course notebooks from this repository. Click on a Notebook to open it.
4. If you instead prefer to use the terminal, remember to relaunch all your terminal windows after the installation. Then refer to [this guide](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html). Most likely the Anaconda installer already created a Python environment for you. But, to have them at hand, the most basic commands are:
    - `conda create -n myenv python=3.11 anaconda` which will create an environment named `myenv` and install the libraries in the anaconda distribution into it (handy to have most of the popular stuff at the ready).
    - `conda activate myenv`.
    - `conda deactivate`.
    - `conda remove --name myenv --all` to remove an environment and all its packages.
A Python environment is a specific Python version equipped with all sort of extra libraries you might need. We will use several throughout the course.

### Edupyter

A valid alternative to Anacoda, only for Windows users, is the [Edupyter package](https://www.portabledevapps.net/edupyter.php). Just follow the instructions and let me know should you face any issue.

## Advanced option: Working locally with the terminal

This set-up allows to control code and Python at a lower level. For the purpose of the course, this is not needed nor recommended. You will need:

1. A rudimentary understanding of the terminal. The **terminal** is just an interface to execute commands in an operating system (most often, your local one). Check the Readme for a couple of guides to terminals for beginners, one for Linux/Max and one for Windows.
2. A rudimentary understanding of git and GitHub. **git** is a program to version code, i.e., it allows you to keep track of different versions of your code. See here for a [tutorial](https://git-scm.com/docs/gittutorial). **GitHub** is instead an online service provided by a company, now part of Microsoft, which allows you to have multiple code repositories and interact with them via git. 
3. **Conda** is a cross platform package and environment manager that installs and manages conda packages from the Anaconda repository as well as from the Anaconda Cloud. Which means you will be able to create Python environments and install packages into them. Some packages we will use might not be in the Anaconda Cloud, in that case you can rollback to using `pip install`. You can use your main Python installation if you like, but it is recommended using conda to keep experiments separated from the OS.

### How to get there

#### Basic terminal commands

For MacOS and Linux:

* `ls` list folder contents
* `cd PATH` move current working directory to the PATH location. `cd ~` for your home folder
* `cd ..` goes up one level in the folder structure
* `touch fun.py` creates an empty file named `fun.py`
* `mv fun.py stuff/` moves `fun/py` to the `stuff` folder, if it exists. If it doesn, `mkdir stuff`

For more, see [here](https://www.makeuseof.com/tag/mac-terminal-commands-cheat-sheet/).

For Windows, see instead [here](https://www.thomas-krenn.com/en/wiki/Cmd_commands_under_Windows).

#### Working on your own copy of the course repository

##### The ideal way

1. The first time, clone the repository locally using `git clone https://github.com/Giovanni1085/UNIBO_Programmazione_LM.git`.
2. Keep getting updates to the code before every lab by going to your local repository directory (e.g., `cd PATH_TO_REPO`) and `git pull`. This will pull all remote changes to local, and update your repository.

##### The easy way - 1 

You might want to use the [GitHub Desktop app](https://desktop.github.com) to keep track of your repositories. If you have it installed, instead of cloning the repo you can use the Open in Desktop option.

##### The easy way - 2

Just download the repository code before every lab, by clicking on `Clone or download`, and then `Download ZIP`. You will then need to unzip the downloaded file.

**IMPORTANT**: Either way, this copy of the course repo will conflict with any change you made yourself to the files in there. This is especially the case for the former way: if you pull, then you edit, then I edit, then you pull again, there will likely be a conflict if we both changed the same files. I recommend to put your edited copies of the repository contents in a separate folder, so to keep your edits (ideally, you could also do versioning on a repository of your own).

## Editors

See the Readme for an indication of the editors you may want to try. Note that you can use Jupyter Notebooks and your Conda Python environment via Visual Studio Code. If you are interested to know more about this option (which is what I use), ask me.