FROM odoo

USER root

# Install pydevd_pycharm
RUN pip3 install pydevd_pycharm
# Optional: Install pydevd-odoo
RUN pip3 install pydevd-odoo
# Add pydevd_pycharm to odoo/__init__.py
RUN echo "import pydevd_pycharm" >> /usr/lib/python3/dist-packages/odoo/__init__.py  \
    && echo "pydevd_pycharm.settrace('host.docker.internal', port=8889, stdoutToServer=True, stderrToServer=True, suspend=False)" >> /usr/lib/python3/dist-packages/odoo/__init__.py

USER odoo
