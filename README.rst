==========
postgresql
==========

Overview
========

This is an Ansible role for installing PostgreSQL on Debian (wheezy or
jessie). It makes sure the installation is done under the locale
en_us.UTF-8. It also installs PostGIS, creates a ``template_postgis``
database template, sets the ``postgres`` password. It assumes the
``duply`` role is also installed, and creates a pre-backup script
that dumps all databases into ``/var/backups``.

Variables
=========

- ``use_timescale``: Default ``false``. Set to ``true`` to install
  Timescale.
- ``postgres_password``: The password of the ``postgres`` database user.
  Store this in the vault. The role sets the ``postgres`` database user
  to have this password.

Meta
====

Written by Antonis Christofides

| Copyright (C) 2014-2015 Antonis Christofides
| Copyright (C) 2014-2021 National Technical University of Athens

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see http://www.gnu.org/licenses/.
