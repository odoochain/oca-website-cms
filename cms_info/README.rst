========
CMS info
========

.. 
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! This file is generated by oca-gen-addon-readme !!
   !! changes will be overwritten.                   !!
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! source digest: sha256:648dcf2d1c547903b18fca4551203e9a4616e16f6a455fe293a5d70cd403fbb7
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

.. |badge1| image:: https://img.shields.io/badge/maturity-Beta-yellow.png
    :target: https://odoo-community.org/page/development-status
    :alt: Beta
.. |badge2| image:: https://img.shields.io/badge/licence-LGPL--3-blue.png
    :target: http://www.gnu.org/licenses/lgpl-3.0-standalone.html
    :alt: License: LGPL-3
.. |badge3| image:: https://img.shields.io/badge/github-OCA%2Fwebsite--cms-lightgray.png?logo=github
    :target: https://github.com/OCA/website-cms/tree/16.0/cms_info
    :alt: OCA/website-cms
.. |badge4| image:: https://img.shields.io/badge/weblate-Translate%20me-F47D42.png
    :target: https://translation.odoo-community.org/projects/website-cms-16-0/website-cms-16-0-cms_info
    :alt: Translate me on Weblate
.. |badge5| image:: https://img.shields.io/badge/runboat-Try%20me-875A7B.png
    :target: https://runboat.odoo-community.org/builds?repo=OCA/website-cms&target_branch=16.0
    :alt: Try me on Runboat

|badge1| |badge2| |badge3| |badge4| |badge5|

Provide basic information for website records / models via `website.published.mixin`.
This module is meant to be used as a base to build your own CMS.

**Table of contents**

.. contents::
   :local:

Usage
=====

New attributes
~~~~~~~~~~~~~~

* ``cms_create_url``: lead to create view. By default ``/cms/create/my.model``
* ``cms_search_url``: lead to search view. By default ``/cms/search/my.model``
* ``cms_edit_url`` (computed field): lead to edit view. By default ``/cms/edit/my.model/model_id``

.. note:: No routing provided.
   This attributes provide only basic information on contents' URLs.
   If you use `cms_form` default routes are handled automatically.
   If not, is up to you to provide your own routes to handle them.


Permission and extra information
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* ``record.cms_is_owner()``: current user is the owner of the record?
* ``record.cms_can_edit()``: current user can edit this record?
* ``record.cms_can_publish()``: current user can publish this record?
* ``record.cms_can_delete()``: current user can delete this record?
* ``model.cms_can_create()``: current user can create a new record?


Info all in one
~~~~~~~~~~~~~~~

When you build CMS UIs you need all those info at once.
This module provides also an helper method `cms_info()`
that gives you back a dictionary containing:

* `is_owner`: True/False,
* `can_edit`: True/False,
* `can_create`: True/False,
* `can_publish`: True/False,
* `can_delete`: True/False,
* `create_url`
* `edit_url`
* `delete_url`

Known issues / Roadmap
======================


Get rid of `website` dependency and move `website.published.mixin` integration
to a glue module.

Changelog
=========

16.0.1.0.0 (2023-05-13)
~~~~~~~~~~~~~~~~~~~~~~~

**Features**

- Migration to v16 (`#127 <https://github.com/OCA/website-cms/issues/127>`_)


13.0.1.0.1 (2021-08-23)
~~~~~~~~~~~~~~~~~~~~~~~

**Features**

- Migration to v13 (`#111 <https://github.com/OCA/website-cms/issues/111>`_)


11.0.1.0.1 (2019-01-18)
~~~~~~~~~~~~~~~~~~~~~~~

**Fixes**

- Info dict default to None values
- Test coverage 100%


11.0.1.0.0 (2018-04-27)
~~~~~~~~~~~~~~~~~~~~~~~

**Improvements**

- Initial release

Bug Tracker
===========

Bugs are tracked on `GitHub Issues <https://github.com/OCA/website-cms/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us to smash it by providing a detailed and welcomed
`feedback <https://github.com/OCA/website-cms/issues/new?body=module:%20cms_info%0Aversion:%2016.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Do not contact contributors directly about support or help with technical issues.

Credits
=======

Authors
~~~~~~~

* Camptocamp

Contributors
~~~~~~~~~~~~

* Simone Orsi <simone.orsi@camptocamp.com>

Maintainers
~~~~~~~~~~~

This module is maintained by the OCA.

.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

This module is part of the `OCA/website-cms <https://github.com/OCA/website-cms/tree/16.0/cms_info>`_ project on GitHub.

You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute.
