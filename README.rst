Plone 5 on Zope 4
=================

Demo of Plone running on Zope 4.

.. note::
    Zope 4.0a1 removed ``bobobase_modification_time`` from ``Persistence.Persistent``. If you want to install Plone 5 on Zope 4, you have to open the ``@@plone-addsite`` script directly. The ZMI is currently broken - probably because of Products.ExternalEditor.

.. warning::
    Don't use this in production!

For more information one Zope 4 see: https://github.com/zopefoundation/Zope


Prerequisites
-------------
- Python 2.7
- Python Virtualenv
- Git


Install
-------

::

    $ git clone git@github.com:collective/minimalplone5.git
    $ cd minimalplone5
    $ virtualenv .
    $ ./bin/pip install zc.buildout
    $ ./bin/buildout

In any case you will be asked for an administrative username and password.

Fire up Zope::

    $ ./bin/instance start

Point your webbrowser to http://localhost:8080/@@plone-addsite (username admin, password admin)
and install a Plone instance.

That's all, folks.
