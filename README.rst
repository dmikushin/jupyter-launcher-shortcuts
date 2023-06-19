==========================
Jupyter Launcher Shortcuts
==========================

Extensions for JupyterLab and classic Jupyter Notebook to add
**user defined** 'launcher' shortcuts. Primarily useful in 
JupyterHub / Binder situations.

For JupyterLab, they're added in the launcher interface.

.. image:: labextension.png

For classic Jupyter Notebook, they are added under the 'New' button

.. image:: nbextension.png

Installation
============

This extension is not updated by its original author for a long time.
Therefore, the best option is to build and install it from source:

.. code:: bash

   pip install .

Upon successfull installation, `@jupyterlab/launcher_shortcuts` should appear in the list:

.. code:: bash

   jupyter labextension list
   JupyterLab v3.6.4
   /opt/conda/share/jupyter/labextensions
        @jupyterlab/launcher_shortcuts v3.0.1 enabled OK (python, jupyterlab_launcher_shortcuts)

Maybe one day the other could have time to make a new release,
then you should be able to install extension simply by doing:

.. code:: bash

   pip install jupyter-launcher-shortcuts

The JupyterLab extension needs to be installed separately.

.. code:: bash

   jupyter labextension install jupyterlab-launcher-shortcuts

Configuring
===========

The extension can be configured in a ``jupyter_notebook_config.py``
file created in any of the directories under ``config`` in the 
output of ``jupyter --paths`` command.

.. code:: python
   
   c.LauncherShortcuts.shortcuts = {
       'my-shiny-application': {
           'title': 'Human Readable Shortcut Title',
           'target': '{base_url}shiny/my-shiny-application-directory/',
           'icon_path': '/path/to/svg/file'
       }
   }
