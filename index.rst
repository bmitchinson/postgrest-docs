.. title:: PostgREST Documentation

.. figure:: _static/logo.png

.. image:: https://img.shields.io/github/stars/postgrest/postgrest.svg?style=social
  :target: https://github.com/PostgREST/postgrest

.. image:: https://img.shields.io/github/release/PostgREST/postgrest.svg
  :target: https://github.com/PostgREST/postgrest/releases

.. image:: https://img.shields.io/docker/pulls/postgrest/postgrest.svg
  :target: https://hub.docker.com/r/postgrest/postgrest/

.. image:: https://img.shields.io/badge/gitter-join%20chat%20%E2%86%92-brightgreen.svg
  :target: https://gitter.im/begriffs/postgrest

.. image:: https://img.shields.io/badge/Donate-Patreon-orange.svg?colorB=F96854
  :target: https://www.patreon.com/postgrest

.. image:: https://img.shields.io/badge/Donate-PayPal-green.svg
  :target: https://www.paypal.me/postgrest

|

PostgREST is a standalone web server that turns your PostgreSQL database directly into a RESTful API. The structural constraints and permissions in the database determine the API endpoints and operations.

Sponsors
--------

.. image:: _static/cybertec.png
  :target: https://www.cybertec-postgresql.com/en/
  :width:  13em

.. image:: _static/2ndquadrant.png
  :target: https://www.2ndquadrant.com/en/?utm_campaign=External%20Websites&utm_source=PostgREST&utm_medium=Logo
  :width:  13em

.. image:: _static/retool.png
  :target: https://tryretool.com/?utm_source=sponsor&utm_campaign=postgrest
  :width:  13em

Motivation
----------

Using PostgREST is an alternative to manual CRUD programming. Custom API servers suffer problems. Writing business logic often duplicates, ignores or hobbles database structure. Object-relational mapping is a leaky abstraction leading to slow imperative code. The PostgREST philosophy establishes a single declarative source of truth: the data itself.

Declarative Programming
-----------------------

It's easier to ask PostgreSQL to join data for you and let its query planner figure out the details than to loop through rows yourself. It's easier to assign permissions to db objects than to add guards in controllers. (This is especially true for cascading permissions in data dependencies.) It's easier to set constraints than to litter code with sanity checks.

Leak-proof Abstraction
----------------------

There is no ORM involved. Creating new views happens in SQL with known performance implications. A database administrator can now create an API from scratch with no custom programming.

One Thing Well
--------------

PostgREST has a focused scope. It works well with other tools like Nginx. This forces you to cleanly separate the data-centric CRUD operations from other concerns. Use a collection of sharp tools rather than building a big ball of mud.

Getting Support
----------------

The project has a friendly and growing community. Join our `chat room <https://gitter.im/begriffs/postgrest>`_ for discussion and help. You can also report or search for bugs/features on the Github `issues <https://github.com/begriffs/postgrest/issues>`_ page.

.. toctree::
   :glob:
   :reversed:
   :caption: Release Notes
   :titlesonly:
   :hidden:

   releases/*

Tutorials
---------

Are you new to PostgREST? This is the place to start!

.. toctree::
   :glob:
   :caption: Tutorials
   :hidden:

   tutorials/*

- :doc:`tutorials/tut0`
- :doc:`tutorials/tut1`

Also have a look at :doc:`Installation <install>` and :ref:`community_tutorials`.

Reference guides
----------------

Technical references for PostgREST's functionality.

.. toctree::
   :caption: API
   :hidden:

   api.rst

.. toctree::
   :caption: Configuration
   :hidden:

   configuration.rst

- :doc:`API <api>`
- :doc:`configuration`

.. _how_tos:

How-to guides
-------------

These are recipes that'll help you address specific use-cases.

.. toctree::
   :glob:
   :caption: How-to guides
   :hidden:

   how-tos/*

- :doc:`how-tos/casting-type-to-custom-json`
- :doc:`how-tos/embedding-table-from-another-schema`
- :doc:`how-tos/providing-images-for-img`

Topic guides
------------

Explanations of some key concepts in PostgREST.

.. toctree::
   :caption: Authentication
   :hidden:

   auth.rst

.. toctree::
   :caption: Installation
   :hidden:

   install.rst

.. toctree::
   :caption: Administration
   :hidden:

   admin.rst

.. toctree::
   :caption: Best Practices
   :hidden:

   best_practices.rst

- :doc:`Authentication <auth>`
- :doc:`Installation <install>`
- :doc:`Administration <admin>`
- :doc:`Best Practices <best_practices>`

Ecosystem
---------

PostgREST has a growing ecosystem of examples, libraries, and experiments. Here is a selection.

.. toctree::
   :caption: Ecosystem
   :hidden:

   ecosystem.rst

* :ref:`eco_example_apps`
* :ref:`eco_external_notification`
* :ref:`eco_extensions`
* :ref:`clientside_libraries`
* :ref:`eco_commercial`

Release Notes
-------------

Here we'll include the most relevant changes so you can migrate to newer versions easily.
You can see the full changelog of each release in the `PostgREST repository <https://github.com/PostgREST/postgrest/releases>`_.

- :doc:`releases/v6.0.2`
- :doc:`releases/v5.2.0`

In Production
-------------

Here are some companies that use PostgREST in production.

* `Sompani <https://www.sompani.com/>`_
* `Datrium <https://www.datrium.com>`_
* `Nimbus <https://nimbusforwork.com/>`_
  - See how Nimbus uses PostgREST in `Paul Copplestone's blog post <https://paul.copplest.one/blog/nimbus-tech-2019-04.html>`_.
* `Catarse <https://www.catarse.me/>`_
* `Moat <https://moat.com/>`_
* `Redsmin <https://www.redsmin.com/>`_
* `Image-charts <https://image-charts.com/>`_
* `MotionDynamic - Fast highly dynamic video generation at scale <https://api.motiondynamic.tech/>`_
* `Drip Depot <https://www.dripdepot.com/>`_
* `Convene <https://info.convene.thomsonreuters.com/en.html>`_ by Thomson-Reuters
* `eGull <http://www.egull.co>`_
* `Elyios <https://elyios.com>`_
* `Simply Connected Systems <https://www.simplyconnectedsystems.com/>`_

.. * `OpenBooking <http://openbooking.ch>`_
.. * `triggerFS - A realtime messaging and distributed trigger system <https://triggerfs.io/>`_

Testimonials
------------

  "It's so fast to develop, it feels like cheating!"

  -- François-G. Ribreau

  "I just have to say that, the CPU/Memory usage compared to our
  Node.js/Waterline ORM based API is ridiculous.  It's hard to even push
  it over 60/70 MB while our current API constantly hits 1GB running on 6
  instances (dynos)."

  -- Louis Brauer

  "I really enjoyed the fact that all of a sudden I was writing
  microservices in SQL DDL (and v8 javascript functions). I dodged so
  much boilerplate. The next thing I knew, we pulled out a full rewrite
  of a Spring+MySQL legacy app in 6 months. Literally 10x faster, and
  code was super concise. The old one took 3 years and a team of 4
  people to develop."

  -- Simone Scarduzio

  "I like the fact that PostgREST does one thing, and one thing well.
  While PostgREST takes care of bridging the gap between our HTTP server
  and PostgreSQL database, we can focus on the development of our API in
  a single language: SQL. This puts the database in the center of our
  architecture, and pushed us to improve our skills in SQL programming
  and database design."

  -- Eric Bréchemier, Data Engineer, eGull SAS

  "PostgREST is performant, stable, and transparent. It allows us to
  bootstrap projects really fast, and to focus on our data and application
  instead of building out the ORM layer. In our k8s cluster, we run a few
  pods per schema we want exposed, and we scale up/down depending on demand.
  Couldn't be happier."

  -- Anupam Garg, Datrium, Inc.

Translations
------------

* `Chinese <http://postgrest.org/zh/latest/>`_ (latest version ``v0.4.2.0``)
