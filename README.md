Python Tutor -- http://pythontutor.com/ -- helps people overcome a fundamental barrier to learning programming: understanding what happens as the computer executes each line of a program's source code. Using this tool, you can write Python, Java, JavaScript, TypeScript, Ruby, C, and C++ programs in your Web browser and visualize what the computer is doing step-by-step as it executes those programs.


### Release Notes for Python Tutor v5.1

- New Features
  - Added aria-label tags to code lines to increase effectiveness of screen readers.
  - Added aria-label tags to data structures and stack frames to increase effectiveness of screen readers.
- Bug Fixes
  - Tab indices on elements are accurate and allow easier tab navigation.
- Known Bugs
  - Not all symbols have mappings.


### Installation Instructions
Note: As our project is simply cosmetic modifications on an existing website, the installation instructions are identical to those of the website itself, so the instructions below are identical to the previously-existing installation instructions.


Pre-requisites:

This tool should be agnostic to software/hardware configuration. It requires web access to maintain a website.

Dependent libraries:

typescript 2.1.6

webpack 2.2.1

Download instructions:

Currently the code can be downloaded from our [team Github repo](https://github.com/Rephraim/junior-design). After handoff the code will reside on the main Python Tutor repo, assuming Philip Guo, the maintainer of the Python Tutor website, chooses to pull our changes into [the main repo](https://github.com/pgbovine/OnlinePythonTutor/).

Installation instructions:

To get started, install:

1.) Node.js / npm

2.) Global npm dependency installs (run these commands in the v5-unity/ directory):

```
sudo npm install webpack -g
npm link webpack            # link to the local node_modules/ dir
sudo npm install webpack-dev-server -g
sudo npm install -g typescript
npm link typescript         # link to the local node_modules/ dir
sudo npm install -g tsd
```

3.) Run `npm install` in this directory to install node dependencies

4.) Run `tsd install` in this directory to install TypeScript definition files

5.) Instal bottle.py to run the local webserver (I suppose we could use node too, but oh wells!)
```
sudo pip install bottle
```
6.) Follow ../v5/tests/frontend-regression-tests/README.txt to install
    dependencies for visual regression testing

Run instructions:

After everything has been installed properly

To start the Webpack file watching and compilation environment, run:
```
npm run webpack
```
To start the webserver, run:
```
npm start
```
then visit here to load an HTML page in your browser:
  http://localhost:8003/visualize.html

To make a production (minified, cache-busted) build for deployment, run:
```
npm run production-build
```
