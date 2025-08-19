<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]




<!-- PROJECT LOGO -->
<br />
<h3 align="center">Dave3625 - Lab 0</h3>
<p align="center">
  <a href="https://github.com/DAVE3625/DAVE3625-24H/tree/main/Lab0">
    <img src="img/logo.png" alt="Environment Setup" width="auto" height="auto">
  </a><p align="center">
    An exercise in setting up your Python environment and performing basic python tasks. <br /> This lab will walk you through setting up a Python virtual environment using UV, installing necessary packages, and setting up a Jupyter Notebook for further exercises.
    <br />
    ·
    <a href="https://github.com/DAVE3625/DAVE3625-24H/issues">Report Bug</a>
    ·
    <a href="https://github.com/DAVE3625/DAVE3625-24H/issues">Request Feature</a>
  </p>
</p>


<!-- ABOUT THE LAB -->
## About The Lab

This lab focuses on setting up the necessary environment for AI and data science tasks, followed by a simple python exercise. You'll start by setting up a UV environment, installing essential Python libraries, and setting up Visual Studio Code with Jupyter Notebook for development.


## Part 0: Choice of IDE

We will focus on using Visual studio code during this course.
You are free to use another IDE, just be aware that the TA's may not be able to help you debug eventual issues with your setup.


### 1. Download Visual Studio Code

Download Visual Studio Code from [here].


### 2. Install the Python Extension
Install the official Python extension for Visual Studio Code.


### 3. Install the Jupyter Extension
Install the Jupyter extension for Visual Studio Code from the "Extensions" menu on the left.


## Part 1: Environment Setup

### 1. Download and Install UV

UV is a fast Python package and project manager. Follow the instructions at [UV documentation](https://docs.astral.sh/uv/) to download and install UV.

For most systems, you can install UV using:

**macOS/Linux:**
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**Windows:**
```bash
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
```

Test if UV was installed correctly by typing in your CLI or terminal:
```bash
uv --version
```


### 2. Create a New UV Project

Creating separate environments for different projects keeps everything organized and prevents dependency problems. It makes sure that changes in one project won't create issues in another, which will make your work easier to manage and debug.

**In your terminal move into the Lab0 folder and initialize the UV project:**
```bash
cd Lab0
uv init
```

This will create a `pyproject.toml` file and a virtual environment for your project.


Creating separate environments for different projects/labs keeps everything organized and prevents dependency problems. It makes sure that changes in one project won't create issues in another, which will make your work easier to manage and debug.


### 3. Activate the Environment

UV automatically manages virtual environments. To work with your project:

```bash
source .venv/bin/activate
```


### 4. Install Python Packages

You can install Python packages (pandas, numpy, matplotlib, scipy, jupyter notebook, ipykernel) using:

```bash 
uv add pandas numpy matplotlib scipy jupyter ipykernel
```


### 7. Create a New Jupyter Notebook
Create a new Jupyter Notebook by creating a file with a .ipynb extension (e.g., new_notebook.ipynb).


### 8. Open the Notebook in VSCode
Open the notebook file in Visual Studio Code and select the UV environment Python interpreter in the top right.


## Part 2: Python Exercises

### Task 1: "Hello World!"

Write and run a Python program that prints `Hello World!`.

1. Create a new Python file or open a Jupyter Notebook.
2. Write a program that outputs the text `'Hello World!'` to the console.
3. Run the program/cell to ensure it executes correctly.

### Task 2: Basic Arithmetic

Perform basic arithmetic operations in Python.

1. Write code to:
   - Add two numbers.
   - Multiply two numbers.
   - Divide one number by another.
2. Display the results of each calculation.

### Task 3: Variables

Learn to store and use values in variables.

1. Create variables to store a name and an age.
2. Print the values of the variables in a formatted string.

### Task 4: Loops

Use a loop to repeat an action multiple times.

1. Write a for-loop that iterates over a range of numbers.
2. In each iteration, print a line of text that includes the current iteration number.

### Task 5: Conditional Statements

Implement decision-making in your code using if-else statements.

1. Write an if-statement that checks if a number is greater than 5.
2. Print a message based on whether the condition is true or false.## Practical Tips

## Additional information

#### 1. **Why Use UV?**
   - **UV** is significantly faster than conda and pip for package installation and environment management.
   - It provides better dependency resolution and handles Python version management automatically.
   - UV creates isolated environments by default, preventing dependency conflicts.

#### 2. **Verifying UV Installation**
   - After installing, verify that UV is installed correctly by typing `uv --version` in your terminal. If the command is not recognized, restart your terminal or check your PATH settings.

#### 3. **Managing Project Dependencies**
   - UV uses `pyproject.toml` files to manage dependencies, which is the modern Python standard.
   - Use `uv add package_name` to add dependencies and `uv remove package_name` to remove them.

#### 4. **Python Version Management**
   - UV can automatically install and manage Python versions. Use `uv python install 3.11` to install Python 3.11.
   - Projects can specify their Python version requirements in `pyproject.toml`.

#### 5. **Lockfiles for Reproducibility**
   - UV generates `uv.lock` files that ensure reproducible installations across different systems.
   - Always commit both `pyproject.toml` and `uv.lock` to version control.

#### 6. **Interpreter Selection in VS Code**
   - After opening a Jupyter Notebook in VS Code, ensure you select the correct Python interpreter from the UV environment in the top right corner to avoid import errors.
   - The interpreter path will typically be in `.venv/bin/python` or `.venv/Scripts/python.exe` (Windows).## Useful UV Commands

## Useful commands

#### 1. **Basic UV Commands**
   - **Check UV Version:**
     ```bash
     uv --version
     ```
   - **Update UV:**
     ```bash
     uv self update
     ```

#### 2. **Project Management**
   - **Initialize a New Project:**
     ```bash
     uv init myproject
     ```
   - **Initialize in Current Directory:**
     ```bash
     uv init
     ```
   - **Sync Dependencies (like activating environment):**
     ```bash
     uv sync
     ```
   - **Run Commands in the Project Environment:**
     ```bash
     uv run python script.py
     uv run jupyter notebook
     ```

#### 3. **Installing and Managing Packages**
   - **Add a Package:**
     ```bash
     uv add package_name
     ```
   - **Add Multiple Packages:**
     ```bash
     uv add package1 package2
     ```
   - **Add a Specific Version of a Package:**
     ```bash
     uv add "package_name==2.1"
     ```
   - **Add Development Dependencies:**
     ```bash
     uv add --dev pytest black
     ```
   - **Remove a Package:**
     ```bash
     uv remove package_name
     ```
     
#### 4. **Python Version Management**
   - **Install a Python Version:**
     ```bash
     uv python install 3.11
     ```
   - **List Available Python Versions:**
     ```bash
     uv python list
     ```
   - **Set Python Version for Project:**
     ```bash
     uv python pin 3.11
     ```

#### 5. **Miscellaneous Commands**
   - **List All Installed Packages:**
     ```bash
     uv tree
     ```
   - **Show Project Information:**
     ```bash
     uv info
     ```
   - **Lock Dependencies:**
     ```bash
     uv lock
     ```
   - **Clean Cache:**
     ```bash
     uv cache clean
     ```

## License
Distributed under the MIT License. See `LICENSE` for more information.

<!-- MARKDOWN LINKS & IMAGES --> 
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[issues-shield]: https://img.shields.io/github/issues/umaimehm/Intro_to_AI_2021.svg?style=for-the-badge
[issues-url]: https://github.com/DAVE3625/Dave3625-Host-2025/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/DAVE3625/DAVE3625-Host-2025/blob/main/Lab0/LICENSE
[here]: https://code.visualstudio.com/
