# Python-M2
Python installation process for MacBook Pro chip M2 silicon 
This is the method that I used for the issue in the installation of Python 3.12.1 in my MacBook Pro M2.
The source of the issue was the python version of the miniconda3 previous installed in my mac (by me) that I forgot that it was there. 
The oldest version installed with the miniconda pkg. was py 3.11.0
This make a bug in the recognizion of the newest version of python (3.12.1) installed with Homebrew and manual. My Mac don't recognized the new python version cause of the oldest already installed. 
So, I solve that problem following this steps:

#1 Descargue Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
brew install pyenv
(echo; echo 'eval "$(/opt/homebrew/bin/brew shellenv)"') >> /Users/yalianachichaco/.zprofile  
    eval "$(/opt/homebrew/bin/brew shellenv)"
brew shellenv   
$ brew                         
brew install pyenv  
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv virtualenv-init -)"

#2 Install Python 'pyenv' in zsch with $brew
pyenv install --list  
pyenv install 3.12.1  
pyenv global 3.12.1  
pyenv local 3.12.1  
python3 --version 

#3 Ejecuted Python 3.12.1
Phyton3
