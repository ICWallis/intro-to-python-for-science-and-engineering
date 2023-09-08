# Intro to Python for Science and Engineering

In-person workshops designed to get scientists and engineers started with Python. 


## Setup Instructions

Below is a guide for setting up your computer to run Python. Anaconda designed to make this process easy for scientists, engineers and others to start using with Python, so use it if you can. 

Anaconda is free to use for students and people doing individual projects. People who work in large corporations need to buy a license to use Anaconda or use Miniconda. The start of Rob's [introduction to Python](https://www.youtube.com/watch?v=wF9ZlPOCwIc&t=193s) describes how to use miniconda. Because it is lightweight, Miniconda may also be a better option for people who already code in another language and are comfortable with working in the terminal and managing requirements.

__Download this tutorial__ from GitHub (you're here now), use the green 'code' button (near the top, right) to download these files as a zip. This set of files hosted on GitHub is referred to as a 'repository' or 'repo'. Unzip the repository somewhere on your computer that is easy to find and is not buried too deep in your file system. I recommend your Documents folder.

__Download and install [Anaconda distribution](https://www.anaconda.com/products/distribution)__ (previously called individual edition). When prompted, accept the default installation settings. For more information on installation, see [this for Windows](https://docs.anaconda.com/anaconda/install/windows/) or for [this for Mac](https://docs.anaconda.com/anaconda/install/mac-os/).

[This video](https://www.youtube.com/watch?v=FdatS_NKVrM) is a couple of years old, but still nicely demonstrates the Anaconda download process and how to work with the terminal/anaconda prompt. Note that the Anaconda website has changed, but the steps are still the same.

__nb conda kernel__ was used in earlier versions of python (before Python 3.9) to automatically create a "kernel" when you make a new environnement. A kernel is what enables you to do interactive programming in Jupyter Lab or Jupyter. VS Studio Code can use an environment to make a kernel on the fly. As described in the video above, nb conda kernel was installed into the base environment. Since Python 3.9, this approach does not work. Instead, we need to create a kernel in environment after that environment has been made. Instructions for how to do this are below, after we have created and activated our environment. 

__Create an environment__ Using Python typically involves assembling existing code that has been released as 'packages'. An environment is a walled garden that contains all of the packages you need for a given project (referred to as the 'requirements' or 'dependencies'). The requirements for this workshop are listed in the environment.yml file. 

The Anaconda "base" environment comes with most of the standard python packages required for science and engineering. The Miniconda does not. It is best practice to make a new environment that is bespoke to your project, rather than adding packages to your base environment. 

In Windows, open the anaconda prompt. In macOS, open a terminal or anaconda prompt. Use the prompt/terminal to navigate to where you have saved this repository (hint: use _cd \<path_to_the_repository\>_ to change directory). [This tutorial and video](https://medium.com/geekculture/basic-bash-commands-c54933183c89) demo's how to navigate with the prompt/terminal.

For people on Windows who already use and prefer powershell: Close powershell. Open anaconda prompt from the start menu. Run _$ conda init powershell_. Reopen powershell and conda should be there. You can now manage environments from powershell like you would from anaconda prompt. 
 
Once you have navigated into the repository folder, you will find the environment.yml file (hint: use _ls_ in MacOS or _dir_ in Windows to list files in your current directory). We will use this file to create an environment that contains the packages needed during the workshop. Execute the following command in the prompt/terminal to create the environment:
 
    $ conda env create -f environment.yml
 
This will take a few minutes and will see a lot of text scroll past in the the prompt/terminal. You may need to respond y then press ENTER if asked to do so. The environment is automatically named sgw_env. Once it has built, we need to activate the environment by executing:
 
    $ conda activate workshop_env
 
\(workshop_env\) should now appear at the start of your current line in the prompt/terminal window.

Refer to [this page](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) for mor information on making and managing conda environments.

__Make a kernel__ As described above, a kernel is what enables interactive programming in the Jupyter environment. After you have activated your environnement, execute the following to create your kernel:

    $ python -m ipykernel install --name workshop_env --display-name "workshop_env" --user

Refer to 'Cheat_sheet__env_and_kernels.txt' for more detail on managing kernels and environments. 

__Open the jupyter notebook called 'Code-along.ipynb'.__ Because the previous step put you inside the right environment (conda activate sgw_env), you can now launch the Jupyter lab IDE (interactive development environnement, where you will write/run code). You are also in the correct folder to start (i.e., the same folder as the notebook you want to open). Into your terminal/prompt type the following and hit return:

    $ jupyter lab
 
This command will launch Jupyter Lab inside your default browser application. Jupyter Lab will run on any modern browser (e.g., firefox, chrome), but may have issues with historic browsers (e.g., safari).

__Missing packages__ If you are missing a package, you can install it on the fly.

To install an additional package into the active environment. Make sure you have activated the environment you want to install your package in.

    $ pip install <PackageName>

__When you are finished__ with Juypter Lab, close the browser window and go back to the prompt/terminal to 'kill the process'. This is done by clicking on the prompt/terminal and typing CTRL + C.

When you come back to the workshop material at a later date, you may have to activate the sgw_env environment again before launching Juypter Lab. 

You can make environments and launch jupyter lab (other code editors) using the Anaconda "navigator" software. However, I strongly recommend you take the time to get familiar with using the prompt/terminal. On the long term, it is a more flexible and useful place to work. 