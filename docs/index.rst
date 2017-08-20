
.. include:: links.rst

===================
iuem20.contenttypes
===================


Adapatation des ``buildout.cfg``

Modification de la version de plone ::

   extends = http://dist.plone.org/release/5.0.8/versions.cfg


ajout des lignes ::
   sources = sources
   auto-checkout =
      plonetheme.iuem20
   
   always-checkout = False
   [sources]
   plonetheme.iuem20 = fs plonetheme.iuem20 path=..

dans section [instance], ajout des modules::

   eggs =
       ..
       plone.reload
       plonetheme.iuem20
       plone.reload
       ..

   environment-vars =
       zope_i18n_compile_mo_files true

correction de la version de flake8 ::

   # flake8 = 3.0.4
   flake8 = 3.3.0

ajout de .settings dans .gitignore


