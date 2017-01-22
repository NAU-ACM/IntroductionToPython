---
Title: Quick Introduction to Ipython Console and Jupyter Notebook
Author: Enes Kemal Ergin
Date: 12/28/2016
---

# Quick Introduction to Ipython Console and Jupyter Notebook

This article is taken from the Cyrille Rossant's [Post](https://www.packtpub.com/books/content/basics-jupyter-notebook-and-python) on Basics of Jupyter Notebook And Python article. I slightly changed some parts and used the necessary parts.

## Content

1. [Overview](#overview)
2. [Launching the IPython Console](#launching-the-ipython-console)
3. [Launching the Jupyter Notebook](#launching-the-jupyter-console)
4. [About the Notebook](#about-the-notebook)
  - [The Notebook Dashboard](#the-notebook-dashboard)
  - [The Notebook User Interface](#the-notebook-user-interface)
    - [Markdown Cells](#markdown-cells)
    - [Code Cells](#code-cells)
  - [The Notebook Modal Interface]()



### Overview

In this small article, we will see how to use IPython console, Jupyter Notebook. This article will give you a head start for the Introduction to Python course given in Spring 2017.

Originally, IPython provided an enhanced command-line console to run Python code interactively. The Jupyter Notebook is a more recent and more sophisticated alternative to the console. Today, both tools are available, and we recommend that you learn to use both.

Since you have installed Python through Anaconda Distribution, you have both of them installed.

### Launching the IPython Console

To run the IPython console, type ```ipython``` in the terminal. There you can write Python commands and see the results instantly.

![Ipython Console](https://github.com/NAU-ACM/IntroductionToPython/blob/master/images/ipythonSS.png?raw=true)

- The IPython console is most convenient when you have a command-line-based workflow and you want to execute some quick Python commands.
- You can exit the IPython console by typing exit.


### Launching the Jupyter Notebook

To run the Jupyter Notebook, type ```jupyter notebook``` in the terminal. This will start the Jupyter server and open a new window in your browser (if that's not the case, go to the following URL: http://localhost:8888).

![Jupyter Notebook](https://github.com/NAU-ACM/IntroductionToPython/blob/master/images/jupyterSS.png?raw=true)

- The Notebook is most convenient when you start a complex analysis project that will involve a substantial amount of interactive experimentation with your code.
- Other common use-cases include keeping track of your interactive session (like a lab notebook), or writing technical documents that involve code, equations, and figures.
- To close the Notebook server, go to the terminal where you launched the server from, and press ```Ctrl + C```. You may need to confirm with ```y```.

### About the Notebook

Now we know how to access the IPython console and the Jupyter Notebook, let's talk more about the notebook and it's features.

#### The Notebook Dashboard

The notebook dashboard is the first page opened when you type ```jupyter notebook```, it has several tabs which are as follows:

- __Files__: shows all files and notebooks in the current directory
- __Running__: shows all kernels currently running on your computer
- __Cluster__: lets you launch kernels for parallel computing
- __Conda__: special for anaconda distribution and gives flexibility for conda environments

---

- A __notebook__ is an interactive document containing code, text, and other elements. A notebook is saved in a file with the ```.ipynb``` extension. This file is a plain text file storing a JSON data structure.
- A __kernel__ is a process running an interactive session. When using IPython, this kernel is a Python process. There are kernels in many languages other than Python.
- In Jupyter, notebooks and kernels are strongly separated. A notebook is a file, whereas a kernel is a process.

#### The Notebook User Interface

To create a new notebook, click on the __New__ button, and select __Notebook (Python [default])__. A new browser tab opens and shows the Notebook interface as follows:

![user interface ](https://www.packtpub.com/sites/default/files/Article-Images/B01727_03.png)

Here are the main components of the interface, from top to bottom:

- The __notebook name__, which you can change by clicking on it. This is also the name of the ```.ipynb``` file.
- The __Menu bar__ gives you access to several actions pertaining to either the notebook or the kernel.
- To the right of the menu bar is the __Kernel__ name. You can change the kernel language of your notebook from the __Kernel__ menu.
- The __Toolbar__ contains icons for common actions. In particular, the dropdown menu showing Code lets you change the type of a cell.
- Following is the main component of the User Interface: the actual Notebook. It consists of a linear list of cells. We will detail the structure of a cell in the following sections.

#### Structure of a Notebook Cell

There are two main types of cells: Markdown cells and code cells, and they are described as follows:

- A ```Markdown cell``` contains rich text. In addition to classic formatting options like bold or italics, we can add links, images, HTML elements, LaTeX mathematical equations, and more.

- A ```code cell``` contains code to be executed by the kernel. The programming language corresponds to the kernel's language. We will only use Python in this book, but you can use many other languages.

You can change the type of a cell by first clicking on a cell to select it, and then choosing the cell's type in the toolbar's dropdown menu showing Markdown or Code.

##### Markdown Cells

![Markdown Cells in Notebook ](https://www.packtpub.com/sites/default/files/Article-Images/B01727_04.png)

The top panel shows the cell in edit mode, while the bottom one shows it in render mode. The edit mode lets you edit the text, while the render mode lets you display the rendered cell. We will explain the differences between these modes in greater detail in the following section.

##### Code Cells

![Code Cells in Notebook ](https://www.packtpub.com/sites/default/files/Article-Images/B01727_05.png)

This code cell contains several parts, as follows:

- The __Prompt number__ shows the cell's number. This number increases every time you run the cell. Since you can run cells of a notebook out of order, nothing guarantees that code numbers are linearly increasing in a given notebook.
- The __Input area__ contains a multi-line text editor that lets you write one or several lines of code with syntax highlighting.
- The __Widget area__ may contain graphical controls; here, it displays a slider.
- The __Output area__ can contain multiple outputs, here:
  - Standard output (text in black)
  - Error output (text with a red background)
  - Rich output (an HTML table and an image here)


#### The Notebook Modal Interface

The Notebook implements a modal interface similar to some text editors such as vim. Mastering this interface may represent a small learning curve for some users.

- Use the __edit mode__ to write code (the selected cell has a green border, and a pen icon appears at the top right of the interface). Click inside a cell to enable the edit mode for this cell (you need to double-click with Markdown cells).
- Use the __command mode__ to operate on cells (the selected cell has a gray border, and there is no pen icon). Click outside the text area of a cell to enable the command mode (you can also press the Esc key).

Keyboard shortcuts are available in the Notebook interface. Type h to show them. We review here the most common ones (for Windows and Linux; shortcuts for Mac OS X may be slightly different).

__Keyboard shortcuts available in both modes__

Here are a few keyboard shortcuts that are always available when a cell is selected:

- ```Ctrl + Enter```: run the cell
- ```Shift + Enter```: run the cell and select the cell below
- ```Alt + Enter```: run the cell and insert a new cell below
- ```Ctrl + S```: save the notebook

__Keyboard shortcuts available in the edit mode__

In the edit mode, you can type code as usual, and you have access to the following keyboard shortcuts:

- ```Esc```: switch to command mode
- ```Ctrl + Shift + -```: split the cell

__Keyboard shortcuts available in the command mode__

In the command mode, keystrokes are bound to cell operations. __Don't write code in command mode or unexpected things will happen!__ For example, typing dd in command mode will delete the selected cell! Here are some keyboard shortcuts available in command mode:

- ```Enter```: switch to edit mode
- ```Up or k```: select the previous cell
- ```Down or j```: select the next cell
- ```y / m```: change the cell type to code cell/Markdown cell
- ```a / b```: insert a new cell above/below the current cell
- ```x / c / v```: cut/copy/paste the current cell
- ```dd```: delete the current cell
- ```z```: undo the last delete operation
- ```Shift + =```: merge the cell below
- ```h```: display the help menu with the list of keyboard shortcuts


Spending some time learning these will give you efficiency.
