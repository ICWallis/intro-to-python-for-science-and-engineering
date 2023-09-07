# Intro to Python for Science and Engineering

In-person workshops designed to get scientists and engineers started with Python. 


## Setup Instructions

You will need to set up your computer before the workshop by following guide below. Anaconda designed to make it easy for scientists, engineers and others to start using with Python, so use it if you can. 

Anaconda is free to use for students and people doing individual projects. People who work in large corporations need to buy a license to use Anaconda or use Miniconda. The start of Rob's [introduction to Python](https://www.youtube.com/watch?v=wF9ZlPOCwIc&t=193s) describes how to use miniconda. Because it is lightweight, Miniconda may also be a better option for people who already code in another language and are comfortable with working in the terminal and managing requirements.

__Download this tutorial__ from GitHub (you're here now), use the green 'code' button (near the top, right) to download these files as a zip. This set of files hosted on GitHub is referred to as a 'repository' or 'repo'. Unzip the repository somewhere on your computer that is easy to find and is not buried too deep in your file system. I recommend your Documents folder.

__Download and install [Anaconda distribution](https://www.anaconda.com/products/distribution)__ (previously called individual edition). When prompted, accept the default installation settings. For more information on installation, see [this for Windows](https://docs.anaconda.com/anaconda/install/windows/) or for [this for Mac](https://docs.anaconda.com/anaconda/install/mac-os/).

[This video](https://www.youtube.com/watch?v=FdatS_NKVrM) is a couple of years old, but still nicely demonstrates the Anaconda download process and how to work with the terminal/anaconda prompt. Note that the Anaconda website has changed, but the steps are still the same.

__Install nb conda kernal__ As demonstrated in the video, we should install a package in the Anaconda "base" environment that enables you to use all kernels when running the Jupyter Lab IDE. In Windows, open the anaconda prompt (search for it in the start menu or look under the Anaconda software group). In macOS, open a terminal. The start of the line of text that appears should read '(base)' and this tells you that you are in the 'base' conda environment (more on this later). Type the following command and hit enter to execute the command (hint: do not include the $ sign, just text and copy-paste usually also works): 

    $ conda install nb_conda_kernel

__Create an environment__ Using Python typically involves assembling existing code that has been released as 'packages'. An environment is a walled garden that contains all of the packages you need for a given project (referred to as the 'requirements' or 'dependencies'). The requirements for this workshop are listed in the environment.yml file. 

The Anaconda "base" environment comes with most of the standard python packages required for science and engineering. The Miniconda does not. It is, however, always best to make your own environment that is bespoke to your project. 

In Windows, open the anaconda prompt. In macOS, open a terminal. Use the prompt/terminal to navigate to where you have saved this repository (hint: use _cd \<path_to_the_repository\>_ to change directory). [This tutorial and video](https://medium.com/geekculture/basic-bash-commands-c54933183c89) demo's how to navigate with the prompt/terminal.
 
Once you have navigated into the repository folder, you will find the environment.yml file (hint: use _ls_ in MacOS or _dir_ in Windows to list files in your current directory). We will use this file to create an environment that contains the packages needed during the workshop. Execute the following command in the prompt/terminal to create the environment:
 
    $ conda env create -f environment.yml
 
This will take a few minutes and will see a lot of text scroll past in the the prompt/terminal. You may need to respond y then press ENTER if asked to do so. The environment is automatically named sgw_env. Once it has built, we need to activate the environment by executing:
 
    $ conda activate workshop_env
 
\(workshop_env\) should now appear at the start of your current line in the prompt/terminal window.

Refer to [this page](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) for mor information on making and managing conda environments.

__Open the jupyter notebook called 'Code-along.ipynb'.__ Because the previous step put you inside the right environment (conda activate sgw_env), you can now launch the Jupyter lab IDE (interactive development environnement, where you will write/run code). You are also in the correct folder to start (i.e., the same folder as the notebook you want to open). Into your terminal/prompt type the following and hit return:

    $ jupyter lab
 
This command will launch Jupyter Lab inside your default browser application. Jupyter Lab will run on any modern browser (e.g., firefox, chrome), but may have issues with historic browsers (e.g., safari).

__When you are finished__ with Juypter Lab, close the browser window and go back to the prompt/terminal to 'kill the process'. This is done by clicking on the prompt/terminal and typing CTRL + C.

When you come back to the workshop material at a later date, you may have to activate the sgw_env environment again before launching Juypter Lab. 

There are other ways to make environments and launch jupyter lab (or other code editors) using the Anaconda "navigator" software. However, I strongly recommend you take the time to get familiar with using the prompt/terminal. 

 
**Other useful Terminal commands**
 
Print a list of your conda environments
  
    $ conda env list
 
Print a list of what is inside your active environment
  
    $ conda list

To install an additional package into the active environment

    $ pip install <PackageName>