Python Tutor -- http://pythontutor.com/ -- helps people overcome a fundamental barrier to learning programming: understanding what happens as the computer executes each line of a program's source code. Using this tool, you can write Python, Java, JavaScript, TypeScript, Ruby, C, and C++ programs in your Web browser and visualize what the computer is doing step-by-step as it executes those programs.

This tool was created by [Philip Guo](http://pgbovine.net/) in January 2010. [See project history](history.txt).

- [Frequently Asked Questions](v3/docs/user-FAQ.md)
- [Overview for Developers](v3/docs/developer-overview.md)

All documentation is viewable online at: https://github.com/pgbovine/OnlinePythonTutor/tree/master/v3/docs

### Release Notes for Python Tutor v5.1

- New Features
-- Added aria-label tags to code lines to increase effectiveness of screen readers.
-- Added aria-label tags to data structures and stack frames to increase effectiveness of screen readers.
- Bug Fixes
-- Tab indices on elements are accurate and allow easier tab navigation.
- Known Bugs
-- Not all symbols have mappings.


### Installation Instructions (as per class requirements)

As our project is simply cosmetic modifications on an existing website, the installation instructions are identical to those of the website itself, so the instructions below are the pre-existing ones.

Pre-requesites:

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

3.) Run "npm install" in this directory to install node dependencies

4.) Run "tsd install" in this directory to install TypeScript definition files

5.) Instal bottle.py to run the local webserver (I suppose we could use node too, but oh wells!)
```
sudo pip install bottle
```
6.) Follow ../tests/frontend-regression-tests/README.txt to install
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

### Quick Start

BY FAR the most preferred way to use Python Tutor is via the official website, since it contains the latest updates: http://pythontutor.com/

You can use [iframe embedding](v3/docs/embedding-HOWTO.md) to easily embed visualizations on your webpage.

If you want to run locally on your own computer, to run Python visualizations try:

```
pip install bottle # make sure the bottle webserver (http://bottlepy.org/) is installed
cd OnlinePythonTutor/v3/
python bottle_server.py
```

You should see the visualizer at: http://localhost:8003/visualize.html

... and the live programming environment at: http://localhost:8003/live.html 

However, it can be hard to run your own visualizer locally for non-Python languages, since there are complex setups in v4-cokapi/ that I haven't yet cleanly packaged up.

For further directions, see [Overview for Developers](v3/docs/developer-overview.md) or explore the [rest of the docs](v3/docs/).


### Acknowledgments

For code or security contributions

- John DeNero - for helping with the official Python 3 port and lots of code patches
- Chris Horne - https://github.com/lahwran - for security tips
- Joshua Landau - joshua@landau.ws - for security tips
- David Wyde - https://davidwyde.com/ - for security tips
- Peter Wentworth and his students - for working on the original Python 3 fork circa 2010/2011
- Brad Miller - for adding pop-up question dialogs to visualizations, and other bug fixes
- David Pritchard and Will Gwozdz - for the Java visualizer and other frontend enhancements
- Peter Robinson - for v3/make_visualizations.py
- Chris Meyers - for custom visualizations such as v3/matrix.py and v3/htmlFrame.py
- Irene Chen - for holistic visualization mode -- v3/js/holistic.js


For general advice and feedback about this project:

- Ned Batchelder
- Jennifer Campbell
- John Dalbey
- John DeNero
- Fredo Durand
- Michael Ernst
- David Evans
- Paul Gries
- Mark Guzdial
- Adam Hartz
- Sean Lip
- Tomas Lozano-Perez
- Bertram Ludaescher
- Brad Miller
- Rob Miller
- Peter Norvig
- Andrew Petersen
- David Pritchard
- Suzanne Rivoire
- Guido van Rossum
- Peter Wentworth
- David Wilkins

... and many, many more!
