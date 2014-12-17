looppulse.web.processing
========================

Loop Pulse Backend Processing

### Setup

1. Install pip, if not yet installed
  
  For mac, `$easy_install pip`

2. Install virtualenv and virtualenvwrapper
  ```
  pip install virtualenv
  pip install virtualenvwrapper
  ```

3. Configure virtualenvwrapper

  Update shell startup script (e.g. ~/.bash_profile) by adding the followings:
  ```
  export WORKON_HOME=$HOME/.virtualenvs
  source /usr/local/bin/virtualenvwrapper.sh
  ```

4. Create a virtual environment for the project
  ```
  mkvirtualenv looppulse.web.processing --python=PATH/TO/PYTHON3
  ```
  For mac, PATH/TO/PYTHON3 looks something like:
  ```
  /Library/Frameworks/Python.framework/Versions/3.4/bin/python3
  ```

5. Start the virtual environment (It's automatically started the first time after mkvirtualenv is executed)
  ```
  workon looppulse.web.processing
  ```

6. Alternatively, pyenv can be used. The tutorial is [here](http://amaral-lab.org/resources/guides/pyenv-tutorial)

### Deployment Development

Follow [heroku toolset](https://devcenter.heroku.com/articles/getting-started-with-python#set-up) and [run the app locally](https://devcenter.heroku.com/articles/getting-started-with-python#run-the-app-locally)

**Everything belows are run inside the project virtual environment!**

### Managing Dependencies
##### Add new packages
Whenever you install a new python package, update the `requirements.txt` file by using the following command:
  ```
  $pip freeze > requirements.txt
  ```

##### Install missing packages
Whenever someone else (other branches) added new packages, update your project by installing the missing packages using the following command:
  ```
  $pip install -r requirements.txt
  ```

