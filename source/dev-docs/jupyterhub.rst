Configuring Jupyterhub at NSLS-II


Python 3 packages installed from PyPI as root:

pip3 install ipython
pip3 install pyzmq
pip3 install mistune
pip3 install jinja2
pip3 install pexpect
pip3 install jsonschema
pip3 install terminado

Python 2 packages installed from PyPI as root:

pip2 install rk==0.2a1
pip2 install pexpect
pip2 install pyzmqI

Python 3 packages installed from source as root:

git clone https://github.com/jupyter/sudospawner
cd sudospawner
pip3 install -e
git clone https://github.com/jupyter/jupyterhub
cd jupyterhub
pip3 install -e

Jupyterhub configuration:

See the SudoSpawner README and wiki for configuring that.
Set the SLL key and certificate.
Set the hub_port to 8081.
Set the port to 7777.
