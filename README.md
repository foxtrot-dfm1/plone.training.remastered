training_buildout
=================

Buildout for the Mastering Plone Training

http://training.plone.org

Buildout uses custom add-on
=================

https://github.com/foxtrot-dfm1/ploneconf.site

Custom Frontend for this projects
=================

-https://github.com/foxtrot-dfm1/plone_training_frontend


Installation guide
=================

-On Ubuntu/Debian, you need to make sure you system is up-to-date:

  sudo apt-get update\
  sudo apt-get -y upgrade

-Then, you need to install the following packages:

  sudo apt-get install python3.9-dev python3.9-tk python3.9-venv build-essential libssl-dev libxml2-dev libxslt1-dev libbz2-dev libjpeg62-dev\
  sudo apt-get install libreadline-dev wv poppler-utils\
  sudo apt-get install git


-On macOS you at least need to install some dependencies with Homebrew

  brew install zlib git readline jpeg libpng libyaml\

- For more information or in case of problems see the official installation instructions.

- Set up Plone like this if you use your own OS (Linux or macOS):

  mkdir training\
  cd training\
  git clone https://github.com/foxtrot-dfm1/plone.training.remastered.git backend\
  cd backend

- Then create a virtual environment with Python 3.9 in the folder backend and install some requirements into it.

  python3.9 -m venv\
  ./bin/pip install -r requirements.txt
 
-Now you can run the buildout for the first time:

  ./bin/buildout

-This will take a long time (~10 minutes on the least powerful Linode) and will produce a lot of output because it downloads and configures more than 260 -Python packages. Once it is done, you can start your Plone instance with the following command.\

  ./bin/instance fg
