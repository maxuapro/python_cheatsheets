## Python Windows + VSC setup cheatsheet
## Python install
## Check versions
Python
```
python --version or
python -V
python -VV
py --version
```
pip
```
pip --version
```
## Virtual environments
#### Create:
Create a folder, cd to the folder, then:
```
python -m venv [virt env name]
```
This creates a [virt env name]folder containing instance of Python
#### Activate:
```
[virt env name]/Scripts/activate
```
and DEactivate: ``` deactivate```
and Delete: ``` rm -r [virt env name] ``` (works for bash)
#### Check out environment
get list of modules:
terminal: ```python``` then:
```py
help("modules")
```
*There is a way to see the only list of modules without dependandant modules...
## Pipenv
install: ```pip install --user pipenv```
Create a folder / cd to the folder / then:
```
pipenv shell
```
this creates an environment with the name of folder
along with the Pipfile (like package.json)
and activates the environment (does it?)
### install modules/packages
install: ```pipenv install [package name]```
uninstall: ```pipenv uninstall [package name]```
install dev dependencies: ```pipenv install [package name] --dev```
see all packages installed + versions ```pipenv graph```
