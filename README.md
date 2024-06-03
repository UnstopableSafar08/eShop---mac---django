# mac
this Project is made up of with Django(python) framework and sqlite as a database and html, css, js as a Frontend.

``` bash
# basic package installatoions
 yum install telnet curl wget net-tools traceroute zip unzip rsync git-all -y


# Conda installation
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh

~/miniconda3/bin/conda init bash # logout/relogin a new shell to reflect the changes | conda deactivate
# e.g. 
# logout
# ssh root@192.168.121.150

~/miniconda3/bin/conda init zsh # logout/relogin a new shell to reflect the changes | conda deactivate
# e.g. 
# logout
# ssh root@192.168.121.150


conda -V
# conda 24.4.0

# conda basic command
conda create --name eshop # my_env_name is eshop
conda activate eshop
conda deactivate
conda env --list
conda env remove --name eshop

# make a latest version of python as a default  
sudo alternatives --config python3.9
python --version
# Python 3.9.18

# eshop app setup
mkdir eshopenv
git clone https://github.com/UnstopableSafar08/eShop---mac---django.git
cd eShop---mac---django/
cd mac/
conda env create -f environment.yml
conda activate eshop
python manage.py makemigrations
python manage.py migrate
python manage.py runserver
python manage.py runserver 0.0.0.0:8000 # python manage.py runserver 192.168.121.150:8000

# Conda and Django initial Setup and Configurations
conda activate your_environment_name    # to activate the existing conda environment  
conda env export > environment.yml      # to generate the environment.yml file that contains all the dependencies packages
conda env create -f environment.yml     # to create a env with all dependencies 
```
