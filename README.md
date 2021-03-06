# Single command for python package creation from one/multiple .py files ( _Make packaging fun again!_ )
[![License: MIT](https://img.shields.io/github/license/Souvic/pypacklib)](https://opensource.org/licenses/MIT)
[![stars](https://img.shields.io/github/stars/Souvic/pypacklib)]()
[![Github All Releases](https://img.shields.io/github/downloads/Souvic/pypacklib/total.svg)]()
[![PyPI](https://img.shields.io/pypi/v/pypacklib)](https://pypi.org/project/pypacklib/)
[![python](https://img.shields.io/github/languages/top/Souvic/pypacklib)]()

[![Build Status](https://scrutinizer-ci.com/g/Souvic/pypacklib/badges/build.png?b=main)](https://scrutinizer-ci.com/g/Souvic/pypacklib/build-status/main)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/Souvic/pypacklib/badges/quality-score.png?b=main)](https://scrutinizer-ci.com/g/Souvic/pypacklib/?branch=main)
[![Release date](https://img.shields.io/github/release-date/Souvic/pypacklib)]()
[![Latest Stable Version](https://img.shields.io/github/v/release/Souvic/pypacklib)]()

[![tweet](https://img.shields.io/twitter/url?style=social&url=https%3A%2F%2Fgithub.com%2FSouvic%2Fpypacklib)](https://twitter.com/intent/tweet?text=I%20found%20this%20awesome%20repo%20on%20GitHub%20%26%20PyPI%20that%20simplifies%20life%20of%20developers%20so%20much!&url=https%3A%2F%2Fgithub.com%2FSouvic%2Fpypacklib)

### Support me


[![Buy Me A Coffee](https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png)](https://www.buymeacoffee.com/Souvic)


Most of the packages are simple and a collection of few functions or classes.
We have created a package for that now that can create python packages, upload to github and distribute to pypi all in a single call.
We collect desired packagename, author name and a few info interactively and create the package from a single python file.
You can use multiple python scripts too.
To use multiple scripts give a space seperated list when asked for file locations with main file (the file where all the functions and classes you want user to use is present) at the start.
For simple packaging, one single file is enough.
- [x] Supports python 3.6+ 
- [x] Autopopulates setup files, README.md and version etc , uploads to GitHub and PyPI
- [x] Easily Customizable
- [x] Easiest to use with only single interactive command
- [ ] 1 min video tutorial

> Fun part: This package is also created by running the script located at src/pypacklib/\_\_main\_\_.py

## Install from PyPi
```
pip3 install pypacklib
```

## Or Install from main branch
```
pip3 install git+https://github.com/Souvic/pypacklib.git
```

# One command to create/upload/update them all!
Easy-to-follow prompts will guide you through the process
```
pypack
```
# Unnecessary detailed instructions (just see the 1 min video)

### To make a new package and upload to github from a some/one python file(s):
1. Run the command _pypack_ (and just follow the interactive framework forgetting the lines\[2,3,4\] written below)
2. Input yes at the first prompt as you will be questioned.
3. Follow the instructions that will appear.
4. Make necessary changes if you have to (e.g. updating README.md file) now on the github repo before submitting to PyPi(by following the upload instruction below)


### To update/upload a package to PyPi which already has a GitHub repo:
1. Make all necessary changes in the python files(location: src/packagename/) in the github repo.
2. Run the command _pypack_ (and just follow the interactive framework forgetting the lines\[2,3,4\] written below)
3. Input no at the first prompt.
4. Follow the instructions that will appear.

# Extras to save GitHub and PyPI passtokens (save typing time)

### Set up your $HOME/.pypirc file with the passtoken like this to save twine password to avoid typing username and password everytime [Doc Link](https://twine.readthedocs.io/en/latest/#keyring-support)
Create $HOME/.pypirc and paste the below code replacing only _yourpasstoken
```
[pypi]
  username = __token__
  password = yourpasstoken
```

### Use git store password utility to avoid typing GitHub username and password everytime [Doc Link](https://git-scm.com/book/en/v2/Git-Tools-Credential-Storage)
Paste the below code for that with your passtoken and username
```
git credential-store --file ~/.mysecretfilelocation store
protocol=https
host=github.com
username=yourusername
password=passtoken
```
## Important note:
You can use
[Github-flavored Markdown](https://guides.github.com/features/mastering-markdown/)
to write your content for your README.md

