# intro-to-python

## Setting up 

### 1. Clone this repo

Open a terminal and go to where you want to keep the repo, then type:
```sh
git clone git@github.com:huang-lab-guelph/intro-to-python.git
```

### 2. Installing Python via pyenv and pyenv-virtualenv:

There are many versions of Python. Even if you only use one of them, 
it is a good idea to isolate the environment (python version, packages, 
etc.) as to not break the defaults installations. 

There are many environment managers, we will use [pyenv](https://github.com/pyenv/pyenv),
together with [pyenv-virtualenv](https://github.com/pyenv/pyenv-virtualenv).
We don't need to do/know much of it, and we will focus only on the very basics here.

---

##### Mac
```sh
brew update
brew install pyenv
```

Add the ```PYENV_ROOT``` variable:
It is a good idea to add an environment variable to the ```PATH```. 
This can easily be done via in a terminal, assuming Zsh, just run:

```sh
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
echo '[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(pyenv init -)"' >> ~/.zshrc
```

for other terminals see [here](https://github.com/pyenv/pyenv?tab=readme-ov-file#set-up-your-shell-environment-for-pyenv>).

Before, the last step, **RESTART THE TERMINAL**. Finally, install pyenv-virtualenv
```shell
brew install pyenv-virtualenv
```

and **RESTART THE TERMINAL**.

#### Windows:
Consider getting a new OS 😞

#### Linux:
We are confident you can figure it out 😏

---

### 2. Creating a new enviroment

It is fairly easy to create an environment now, 
let's create a basic one called python-intro-3.12

```shell
pyenv virtualenv 3.12.5 python-intro
```

note the format

```shell
pyenv virtualenv [PYTHON VERSION] [ENVRIOMENT NAME]
```

to activate the environment we just created we run:

```sh
pyenv activate python-intro
```

By default, your terminal should show the name of the environment in parentheses
as a prefix to the prompt.


More details about pyenv and pyenv-virtualenv can be found the respective sources.

### 3. Installing the required libraries

The following is the list of libraries that we will use. 
We use a requirement.txt file which you already have in the folder where you cloned this repo

```text
notebook # The jupyter notebook to explore data and write simple code
pandas # Manages csv type files and tables
scipy # Scientific library
matplotlib # For creating images and graphs
seaborn # Better visualizations
```

we can install all by running (inside the intro-to-python folder)

```sh
pip install -r requirements.txt
```

We are now ready. From the notebook we can run

```text
jupyter notebook
```