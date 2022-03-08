# How to Create VENV with Virtualwrapper Package

Virtual Environments are a way of separating python packages for individual project.

## Requirements

- Python3 
- virtualwrapper

## Installing Virtualwrapper

```python
sudo pip3 install virtualwrapper
# or
pip3 install virtualwrapper
```

That's all. Easy, right?

## Configure virtualwrapper to load the necessary commands

In your shell startup file (.bashrc, .profile, .zshrc, etc.),

>You can change the **WORKON_HOME** to any directory you like.

```bash
export WORKON_HOME=$HOME/virtualenvs
export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3
source usr/local/bin/virtualenvwrapper.sh
```

If you didn't install the virtualwrapper package as root,

```bash
export WORKON_HOME=$HOME/virtualenvs
export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3
source $HOME/.local/bin/virtualenvwrapper.sh
```

And then, source your shell startup file,

```bash
source ~/.bashrc
```

## Benefits of using **virtualwrapper** over **venv** and Usage

- virtualwrapper keeps all the virtual environments in one place.
  - ```mkvirtualenv  -p [python3.8] [venv-name]```
  - You can specify different python version with option `-p`.
- Easy to activate virtual environments.
  - ```workon [venv-name]```
- Easy to list all virtual environements.
  - ```workon```
- Easy to deactivate virtual environments.
  - ```deactivate```
- Easy to delete.
  - ```rmvirtualenv [venv-name]```
