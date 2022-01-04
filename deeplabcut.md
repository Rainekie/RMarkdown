# instration manual - deeplabcut

## Requirement

- mac (MacBook Pro Retina 13-inch Early 2015, macOS Big Sur[version 11.6])
- homebrew
- python (version 3.8.5)
- pyenv
- pipenv

## Installation

1. Install pyenv

```sh
$ brew update
$ brew install pyenv
```

2. Configure your shell's environment

```sh
$ echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.profile
$ echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.profile
$ echo 'eval "$(pyenv init --path)"' >> ~/.profile
$ echo 'if [ -n "$PS1" -a -n "$BASH_VERSION" ]; then source ~/.bashrc; fi' >> ~/.profile

$ echo 'eval "$(pyenv init -)"' >> ~/.bashrc

$ source ~/.bash_profile
```

For the detailed information, see [here](https://github.com/pyenv/pyenv#basic-github-checkout)

3. Install xz

```sh
$ brew install xz
```

4. Install python in pyenv

```sh
$ env PYTHON_CONFIGURE_OPTS="--enable-framework" pyenv install 3.8.5

$ pyenv local 3.8.5
```

check you could install the desired python version correctly.

```sh
$ python --version
Python 3.8.5
```

5. Install pipenv

```sh
$ pip install pipenv
```

6. Move to (or create) a directry where you want to save deeplabcut

```sh
$ cd <dir>
```

or

```sh
$ mkdir -p <dir>; cd $_ 
```

7. Create a new pipenv project(environment) using python 3.8.5

```sh
$ pipenv --python 3.8.5
```

8. Install deeplabcut on into the project

```sh
$ pipenv install 'deeplabcut[gui]'==2.2.0.3
```

9. Launch deeplabcut gui

```sh
$ pipenv run python -m deeplabcut
```

## Note
Apple Silicon environment (new Macbook pro which has M1 chip series) may not work properly because pyenv or pipenv or deeplabcut might not support the chip.
