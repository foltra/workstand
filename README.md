# Workstand

## Quick Install (Project Setup)

1.  `$ git clone git@github.com:BridgeCityBicycleCoop/workstand.git`
2. `$ cd workstand`
3. `$ brew install pyenv`
4. `$ brew install pipenv`
5. `$ pyenv install 3.6.6`
6. `$ pipenv install --python 3.6.6 --dev`
7. `$ pipenv shell`
8. `$ npm install`
9. `$ ./manage.py migrate`
10. `$ ./manage.py loaddata fixtures.yaml`
11. `$ ./manage.py runserver`
12. `$ npm start` _open a new terminal session to run this in workstand/bikeshop_project_
13. Visit http://localhost:8000/
14. Login with `u: admin@workstand.dev`and `p: bike!bike!`

## Quick Start

1. `$ cd workstand/bikeshop_project`
2. `$ ./manage.py run server`
3. `$ npm start` _open a new terminal session to run this_

## Enable Async Tasks

This is needed for the experimental bike-inventory feature.

### Requirements

1. Docker

### Start a worker process

1. `./manage.py runworker -v3 --settings bikeshop.settings.development check-cpic`

**Requirements**

1. npm
2. pyenv (>= 1.2.11)
3. pipenv (>= 2018.11.26)

## Depency Problems
1. `zipimport.ZipImportError: can't decompress data; zlib not available`
  - Looks like you are missing headers in Mac Os. Following the solution provided in [this StackOverflow solution](stackoverflow.com/questions/52741673/how-can-i-install-zlib-on-mac-os-x-mojave-10-14).