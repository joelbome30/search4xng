.. SPDX-License-Identifier: AGPL-3.0-or-later

.. _SearXNG: https://github.com/searxng/searxng
.. _4get: https://git.lolcat.ca/lolcat/4get
.. _Installation guide: SEARCH4XNG.md
.. _CONTRIBUTING: CONTRIBUTING.rst
.. _LICENSE: LICENSE

.. image:: assets/search4xng-logo.png
   :target: https://github.com/joelbome30/search4xng
   :alt: Search4XNG
   :width: 720px


Search4XNG
==========

Search4XNG is a privacy-respecting metasearch engine built on `SearXNG`_ with
a compact Gruvbox interface inspired by `4get`_. Users are neither tracked nor
profiled.

.. image:: https://img.shields.io/github/license/joelbome30/search4xng?style=flat-square&label=license&color=4b7cff&cacheSeconds=86400
   :target: https://github.com/joelbome30/search4xng/blob/master/LICENSE
   :alt: License

.. image:: https://img.shields.io/github/last-commit/joelbome30/search4xng?style=flat-square&color=4b7cff&cacheSeconds=3600
   :target: https://github.com/joelbome30/search4xng/commits/master/
   :alt: Last commit

.. image:: https://img.shields.io/badge/interface-4get--inspired-00b800?style=flat-square
   :target: https://git.lolcat.ca/lolcat/4get
   :alt: 4get-inspired interface

Features
========

- SearXNG's search engines and privacy controls.
- A responsive, compact interface inspired by 4get.
- Gruvbox colors with light borders and dense search results.
- Ready-to-use Docker Compose configuration with Valkey.
- Example Caddy configuration for HTTPS deployments.

Setup
=====

See the `Installation guide`_ for development, Docker and free 24/7 hosting
instructions.

Contributing
============

See CONTRIBUTING_ for more details. Contributions to the Search4XNG interface
are welcome; contributions to the underlying engine should generally be sent
to upstream SearXNG.

License
=======

Search4XNG is licensed under the GNU Affero General Public License
(AGPL-3.0-or-later). See LICENSE_ for details. SearXNG and 4get retain their
respective copyrights and licenses.
